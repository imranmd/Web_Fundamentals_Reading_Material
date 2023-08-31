Here are several use cases of custom hooks along with sample code and comments to illustrate each scenario:

### 1. Data Fetching

Custom hooks can be used to encapsulate data fetching logic, making it reusable across different components.

```jsx
import { useState, useEffect } from 'react';

// Custom hook for data fetching
function useFetch(url) {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    async function fetchData() {
      try {
        const response = await fetch(url);
        const jsonData = await response.json();
        setData(jsonData);
        setLoading(false);
      } catch (error) {
        console.error('Error fetching data:', error);
      }
    }

    fetchData();
  }, [url]);

  return { data, loading };
}

export default useFetch;
```

### 2. Form Handling

Custom hooks can simplify form handling logic, abstracting away repetitive code.

```jsx
import { useState } from 'react';

// Custom hook for form handling
function useForm(initialState) {
  const [formData, setFormData] = useState(initialState);

  const handleInputChange = (event) => {
    const { name, value } = event.target;
    setFormData((prevData) => ({ ...prevData, [name]: value }));
  };

  return { formData, handleInputChange };
}

export default useForm;
```

### 3. Dark Mode

Custom hooks can encapsulate theme-related logic, allowing for easy implementation of dark mode.

```jsx
import { useState, useEffect } from 'react';

// Custom hook for dark mode
function useDarkMode() {
  const [isDarkMode, setIsDarkMode] = useState(false);

  useEffect(() => {
    // Apply dark mode styles
    if (isDarkMode) {
      document.body.classList.add('dark-mode');
    } else {
      document.body.classList.remove('dark-mode');
    }
  }, [isDarkMode]);

  return { isDarkMode, toggleDarkMode: () => setIsDarkMode(!isDarkMode) };
}

export default useDarkMode;
```

### 4. Local Storage

Custom hooks can manage interactions with browser local storage.

```jsx
import { useState } from 'react';

// Custom hook for local storage
function useLocalStorage(key, initialValue) {
  const [storedValue, setStoredValue] = useState(() => {
    const item = window.localStorage.getItem(key);
    return item ? JSON.parse(item) : initialValue;
  });

  const setValue = (value) => {
    setStoredValue(value);
    window.localStorage.setItem(key, JSON.stringify(value));
  };

  return [storedValue, setValue];
}

export default useLocalStorage;
```

### 5. Debouncing

Custom hooks can handle debounce logic for better performance when dealing with frequent events.

```jsx
import { useState, useEffect } from 'react';

// Custom hook for debounce
function useDebounce(value, delay) {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const handler = setTimeout(() => {
      setDebouncedValue(value);
    }, delay);

    return () => {
      clearTimeout(handler);
    };
  }, [value, delay]);

  return debouncedValue;
}

export default useDebounce;
```

Custom hooks provide a powerful way to encapsulate and share logic across your React components. These examples illustrate the versatility and benefits of custom hooks, from data fetching to handling form inputs, managing themes, and more. Utilize custom hooks to enhance your application's reusability, organization, and performance.