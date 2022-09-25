# Kogane Override Value

![2022-09-25_121231](https://user-images.githubusercontent.com/6134875/192126676-1661460e-ba73-47ee-8745-6dbdeb79df9e.png)

値を上書きするかどうかをトグルで変更できるクラス

## 使用例

```csharp
using Kogane;
using UnityEngine;

public sealed class Example : ScriptableObject
{
    public OverrideValue<Vector3> m_position;

    public void Apply( Transform transform )
    {
        m_position.Override( x => transform.position = x );
    }
}
```

![2022-09-25_121529](https://user-images.githubusercontent.com/6134875/192126680-4bfb0ee3-45ca-47cd-bd12-bf67e8d60bf1.png)
