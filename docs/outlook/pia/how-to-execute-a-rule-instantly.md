---
title: ルールを直ちに実行する
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6bb6ac5422b9785660cb3ec0020c01244002c6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320371"
---
# <a name="execute-a-rule-instantly"></a>ルールを直ちに実行する

この例では、[Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) オブジェクトの [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) メソッドを使用して、ルールを直ちに実行する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

**Rule** オブジェクトの **Execute** メソッドを呼び出すと、仕分けルールを直ちに実行できます。 **Execute** メソッドのパラメーターはオプションです。パラメーターを指定しなかった場合、受信トレイ (サブフォルダーを除く) のすべてのメッセージに仕分けルールが適用され、パラメーターの既定値が使用されます。次の表に、 **Execute** メソッドのオプションのパラメーターの既定値を示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パラメーター</p></th>
<th><p>既定値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowProgress</p></td>
<td><p>誤り</p></td>
</tr>
<tr class="even">
<td><p>フォルダー</p></td>
<td><p>受信トレイ</p></td>
</tr>
<tr class="odd">
<td><p>IncludeSubfolders</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>RuleExecuteOption</p></td>
<td><p>OlRuleExecuteOption.olRuleExecuteAllMessages</p></td>
</tr>
</tbody>
</table>


ルールの実行は、ルールとアラート ウィザードを使用することで取り消しできます。 また、*ShowProgress* パラメーターを **true** に設定して、進行状況ダイアログ ボックスをキャンセルすることでも、ルールの実行を取り消しできます。 進行状況ダイアログ ボックスをキャンセルすると、**Execute** はエラーを返します。

次のコード例の ExecuteManagerRule では、CreateManagerRule プロシージャで作成したルールを取得しています。このプロシージャについては、トピック「[上司からのメール アイテムを分類して確認のフラグを設定する](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)」を参照してください。 その後、ExecuteManagerRule では、ルールが null 参照かどうかを確認します。 ルールが null 参照でない場合は、ExecuteManagerRule から既定のパラメーターでルールの **Execute** メソッドを呼び出して、ルールを直ちに実行します。

> [!NOTE]
> [!メモ] [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) プロパティが **true** を返すかどうかに関係なく、仕分けルールを 1 回適用するには、 **Rule.Execute** メソッドを使用します。現在のセッションおよびそれ以後のセッションに対して仕分けルールを適用するには、 **Rule.Enabled** プロパティと [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) メソッドの両方を使用します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [ルール](rules.md)

