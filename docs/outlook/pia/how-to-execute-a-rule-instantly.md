---
title: ルールを直ちに実行する
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb5de218d11a91410da2512ce3cb7533c1e8b501
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405540"
---
# <a name="execute-a-rule-instantly"></a><span data-ttu-id="1ec54-102">ルールを直ちに実行する</span><span class="sxs-lookup"><span data-stu-id="1ec54-102">Execute a rule instantly</span></span>

<span data-ttu-id="1ec54-103">この例では、[Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) オブジェクトの [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) メソッドを使用して、ルールを直ちに実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-103">This example shows how to execute a rule instantly by using the [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) method of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="1ec54-104">例</span><span class="sxs-lookup"><span data-stu-id="1ec54-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1ec54-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="1ec54-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="1ec54-p101">**Rule** オブジェクトの **Execute** メソッドを呼び出すと、仕分けルールを直ちに実行できます。 **Execute** メソッドのパラメーターはオプションです。パラメーターを指定しなかった場合、受信トレイ (サブフォルダーを除く) のすべてのメッセージに仕分けルールが適用され、パラメーターの既定値が使用されます。次の表に、 **Execute** メソッドのオプションのパラメーターの既定値を示します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-p101">You can cause a rule to execute immediately by calling the **Execute** method on the **Rule** object. The parameters to the **Execute** method are optional; if they are not specified, the rule will be applied to all messages in the Inbox but not to the subfolders of the Inbox, and default values for the parameters will be used. The following table lists the default values for the optional parameters of the **Execute** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ec54-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1ec54-109">Parameter</span></span></p></th>
<th><p><span data-ttu-id="1ec54-110">既定値</span><span class="sxs-lookup"><span data-stu-id="1ec54-110">Default value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ec54-111">ShowProgress</span><span class="sxs-lookup"><span data-stu-id="1ec54-111">ShowProgress Property</span></span></p></td>
<td><p><span data-ttu-id="1ec54-112">False</span><span class="sxs-lookup"><span data-stu-id="1ec54-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec54-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="1ec54-113">Folder</span></span></p></td>
<td><p><span data-ttu-id="1ec54-114">受信トレイ</span><span class="sxs-lookup"><span data-stu-id="1ec54-114">Inbox</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec54-115">IncludeSubfolders</span><span class="sxs-lookup"><span data-stu-id="1ec54-115">IncludeSubfolders</span></span></p></td>
<td><p><span data-ttu-id="1ec54-116">False</span><span class="sxs-lookup"><span data-stu-id="1ec54-116">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec54-117">RuleExecuteOption</span><span class="sxs-lookup"><span data-stu-id="1ec54-117">RuleExecuteOption</span></span></p></td>
<td><p><span data-ttu-id="1ec54-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span><span class="sxs-lookup"><span data-stu-id="1ec54-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ec54-119">ルールの実行は、ルールとアラート ウィザードを使用することで取り消しできます。</span><span class="sxs-lookup"><span data-stu-id="1ec54-119">You can cancel a rule execution by using the Rules and Alerts Wizard.</span></span> <span data-ttu-id="1ec54-120">また、*ShowProgress* パラメーターを **true** に設定して、進行状況ダイアログ ボックスをキャンセルすることでも、ルールの実行を取り消しできます。</span><span class="sxs-lookup"><span data-stu-id="1ec54-120">You can also cancel a rule execution by setting the  *ShowProgress* parameter to **true** and then canceling the progress dialog box.</span></span> <span data-ttu-id="1ec54-121">進行状況ダイアログ ボックスをキャンセルすると、**Execute** はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-121">Once you cancel the progress dialog box, **Execute** will return an error.</span></span>

<span data-ttu-id="1ec54-122">次のコード例の ExecuteManagerRule では、CreateManagerRule プロシージャで作成したルールを取得しています。このプロシージャについては、トピック「[上司からのメール アイテムを分類して確認のフラグを設定する](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ec54-122">In the following code example,   gets the rule that was created in the procedure   from the topic How to: Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up.</span></span> <span data-ttu-id="1ec54-123">その後、ExecuteManagerRule では、ルールが null 参照かどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-123"> then checks whether the rule is not a null reference.</span></span> <span data-ttu-id="1ec54-124">ルールが null 参照でない場合は、ExecuteManagerRule から既定のパラメーターでルールの **Execute** メソッドを呼び出して、ルールを直ちに実行します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-124">If the rule is not a null reference,   calls the Execute method on the rule with default parameters, instantly executing the rule.</span></span>

> [!NOTE]
> <span data-ttu-id="1ec54-p104">[!メモ] [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) プロパティが **true** を返すかどうかに関係なく、仕分けルールを 1 回適用するには、 **Rule.Execute** メソッドを使用します。現在のセッションおよびそれ以後のセッションに対して仕分けルールを適用するには、 **Rule.Enabled** プロパティと [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) メソッドの両方を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-p104">To apply a rule once, regardless of whether the [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) property returns **true**, use the **Rule.Execute** method. To apply the rule for the current session and beyond the current session, use both the **Rule.Enabled** property and the [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) method.</span></span>

<span data-ttu-id="1ec54-127">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ec54-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="1ec54-128">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ec54-128">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="1ec54-129">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1ec54-129">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1ec54-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ec54-130">See also</span></span>

- [<span data-ttu-id="1ec54-131">ルール</span><span class="sxs-lookup"><span data-stu-id="1ec54-131">Rules</span></span>](rules.md)

