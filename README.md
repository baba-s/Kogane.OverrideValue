# Kogane Override Value

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