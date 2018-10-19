---
title: 件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1ff096454aa15a0a45c423913140eb50e6de9678
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406324"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a><span data-ttu-id="f2764-102">件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する</span><span class="sxs-lookup"><span data-stu-id="f2764-102">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>

<span data-ttu-id="f2764-103">この例では、件名に含まれる複数の単語に基づいてメール アイテムに分類項目を割り当てるルールをセットアップする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f2764-103">This example shows how to set up a rule that assigns categories to mail items based on multiple words in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="f2764-104">例</span><span class="sxs-lookup"><span data-stu-id="f2764-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f2764-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="f2764-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f2764-106">Outlook では、編成と表示を簡単にするためにアイテムを項目別に分類できます。</span><span class="sxs-lookup"><span data-stu-id="f2764-106">In Outlook, items can be categorized for easier organization and display.</span></span> <span data-ttu-id="f2764-107">Outlook オブジェクト モデルには、分類項目を表すための [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) オブジェクトと [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) コレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f2764-107">The Outlook object model provides the [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object and the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection to represent categories.</span></span> <span data-ttu-id="f2764-108">Outlook アイテムの **Category** オブジェクトと **Categories** コレクションの詳細については、「[分類項目を列挙および追加する](how-to-enumerate-and-add-categories.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2764-108">For more information about the **Category** object and the **Categories** collection for an Outlook item, see [How to: Enumerate and Add Categories](how-to-enumerate-and-add-categories.md).</span></span>

<span data-ttu-id="f2764-109">[Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) オブジェクトで表されるルールは、複数の条件で割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f2764-109">A rule, represented by a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object, can be assigned with multiple conditions.</span></span> <span data-ttu-id="f2764-110">評価する条件または実行する処理を表す配列を取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="f2764-110">You can get or set an array that represents conditions to be evaluated or actions to be completed.</span></span> <span data-ttu-id="f2764-111">たとえば、 [TextRuleCondition](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) オブジェクトの [Text](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) プロパティは、ルールの条件で評価するテキストを表す文字列要素の配列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f2764-111">For example, the [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) property of the [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) object returns or sets an array of string elements that represents the text to be evaluated by the rule condition.</span></span> <span data-ttu-id="f2764-112">配列には、評価する 1 つ以上の文字列を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f2764-112">You must assign an array with one string or multiple strings for evaluation.</span></span> <span data-ttu-id="f2764-113">配列で割り当てられた複数のテキスト文字列を評価するには、論理和演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="f2764-113">To evaluate multiple text strings that are assigned in an array, use the logical OR operation.</span></span> 

<span data-ttu-id="f2764-114">配列の取得または設定に使用可能なプロパティは、[Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\))、[Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\))、[Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\))、[FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\))、および **TextRuleCondition.Text** です。</span><span class="sxs-lookup"><span data-stu-id="f2764-114">The properties that you can use to get or set an array are as follows: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)) , [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)) , [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)) , [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) , and **TextRuleCondition.Text**.</span></span> <span data-ttu-id="f2764-115">ルールの詳細については、「[上司からのメール アイテムを分類して確認のフラグを設定する](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2764-115">For more information about rules, see [How to: Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span>

<span data-ttu-id="f2764-116">次の例の CreateTextAndCategoryRule では、CategoryExists を使用して、**Categories** コレクション内の "Office" または "Outlook" という名前の分類項目についてユーザーのメール アイテムをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f2764-116">In the following example,   uses the   method to check the user's mail items for any categories by the name "Office" or "Outlook" in the Categories collection.</span></span> <span data-ttu-id="f2764-117">分類項目が見つからない場合は、その分類項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="f2764-117">If no categories are found, they are added.</span></span> <span data-ttu-id="f2764-118">その後、この例では "Office"、"Outlook"、および "2007" を含む文字列の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="f2764-118">The example then creates an array of strings that include "Office, "Outlook", and "2007".</span></span> <span data-ttu-id="f2764-119">この文字列は、評価される条件を表します。</span><span class="sxs-lookup"><span data-stu-id="f2764-119">This array will represent the conditions to be evaluated.</span></span> <span data-ttu-id="f2764-120">さらに、CreateTextAndCategoryRule では、**TextRuleCondition** オブジェクトの **Text** プロパティと [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) コレクションの [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) プロパティを使用して、配列内の条件について件名を調べることで分類項目を割り当てるルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2764-120"> then creates a rule that assigns categories by examining the subject for any of the conditions in the array by using the Text property of the TextRuleCondition object and the BodyOrSubject property of the RuleConditions collection.</span></span> <span data-ttu-id="f2764-121">条件が一致した場合には、 [RuleActions](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) オブジェクトの [AssignToCategory](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) メソッドを使用して、Office および Outlook の分類項目をアイテムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f2764-121">If the condition is satisfied, the categories of Office and Outlook are assigned to the item by using the [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) method of the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) object.</span></span>

<span data-ttu-id="f2764-122">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2764-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f2764-123">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2764-123">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f2764-124">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f2764-124">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f2764-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2764-125">See also</span></span>

- [<span data-ttu-id="f2764-126">ルール</span><span class="sxs-lookup"><span data-stu-id="f2764-126">Rules</span></span>](rules.md)

