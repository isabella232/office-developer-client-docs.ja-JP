---
title: 件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50966b99febe03500feb4b693cfba50819d9b7a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560635"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a>件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する

この例では、件名に含まれる複数の単語に基づいてメール アイテムに分類項目を割り当てるルールをセットアップする方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Outlook では、編成と表示を簡単にするためにアイテムを項目別に分類できます。 Outlook オブジェクト モデルには、分類項目を表すための [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) オブジェクトと [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) コレクションがあります。 Outlook アイテムの **Category** オブジェクトと **Categories** コレクションの詳細については、「[分類項目を列挙および追加する](how-to-enumerate-and-add-categories.md)」を参照してください。

[Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) オブジェクトで表されるルールは、複数の条件で割り当てることができます。 評価する条件または実行する処理を表す配列を取得または設定できます。 たとえば、 [TextRuleCondition](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) オブジェクトの [Text](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) プロパティは、ルールの条件で評価するテキストを表す文字列要素の配列を取得または設定します。 配列には、評価する 1 つ以上の文字列を割り当てます。 配列で割り当てられた複数のテキスト文字列を評価するには、論理和演算子を使用します。 

配列の取得または設定に使用可能なプロパティは、[Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\))、[Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\))、[Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\))、[FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\))、および **TextRuleCondition.Text** です。 ルールの詳細については、「[上司からのメール アイテムを分類して確認のフラグを設定する](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)」を参照してください。

次の例の CreateTextAndCategoryRule では、CategoryExists を使用して、**Categories** コレクション内の "Office" または "Outlook" という名前の分類項目についてユーザーのメール アイテムをチェックします。 分類項目が見つからない場合は、その分類項目が追加されます。 その後、この例では "Office"、"Outlook"、および "2007" を含む文字列の配列を作成します。 この文字列は、評価される条件を表します。 さらに、CreateTextAndCategoryRule では、**TextRuleCondition** オブジェクトの **Text** プロパティと [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) コレクションの [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) プロパティを使用して、配列内の条件について件名を調べることで分類項目を割り当てるルールを作成します。 条件が一致した場合には、 [RuleActions](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) オブジェクトの [AssignToCategory](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) メソッドを使用して、Office および Outlook の分類項目をアイテムに割り当てます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>関連項目

- [ルール](rules.md)

