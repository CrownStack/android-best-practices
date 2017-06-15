

## Nullness Annotation
   @Nullable and @NonNull is use to check the nullness of a variable, parameter and return type.
   
  * `@Nullable` check that it can be null.
  * `@NotNull` check that it can be null.

    ```
    @NonNull
    @Override
    public View onCreateView(String name, @NonNull Context context, @NonNull AttributeSet attrs) {
     ... 
    }
    ```

## Resource Annotation

  * `@StringRes` passing string is a store in string.xml(int resource).
     ```
     public void setTitle(@StringRes int resId) { … }
     ```
  
  * `DrawableRes` passing drawable is int resource
     ```
     private void alert(@DrawableRes int background){ ... }
     ```

## Permission annotations

  * `@RequiresPermission` check the permission in caller method.
    ```
    @RequiresPermission(Manifest.permission.ACCESS_FINE_LOCATION)
    public void getLocation(Context context){ ...};
    ```

  * `allOf` attribute is check all the given permission in caller method.
     ```
    @RequiresPermission(allOf = {
    Manifest.permission.READ_EXTERNAL_STORAGE,
    Manifest.permission.WRITE_EXTERNAL_STORAGE})
    private void openCamera() {
    ...
    }
   ```








