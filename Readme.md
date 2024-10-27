# Blazor Events

### Usage

#### Prevents double click

```csharp
<SafeButton Task="AddCounter">
   Simple Click
</SafeButton>

@code{
    protected int Counter = 0;
    protected async Task AddCounter()
    {
        Counter++;
        StateHasChanged();
        await Task.Delay(500);
    }
}
```
#### Waits for execution to end

You will not be able increment counter before 5 seconds
```csharp
<SafeButton Task="AddCounter" WaitForExecution=true>
   Simple Click
</SafeButton>

@code{
    protected int Counter = 0;
    protected async Task AddCounter()
    {
        Counter++;
        StateHasChanged();
        await Task.Delay(5000);
    }
}
```
#### Customization

```csharp
<SafeButton Task="AddCounter" Class="btn btn-primary" Style="color:red;">
   Simple Click
</SafeButton>
```