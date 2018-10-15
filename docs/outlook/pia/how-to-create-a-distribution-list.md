---
title: 配布リストを作成する
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 19b282a3b3e756814aa2add07cda4be7609206ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407136"
---
# <a name="create-a-distribution-list"></a>配布リストを作成する

この例では、配布リストを作成してそれをユーザーに表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


次のコード例の CreateDistributionList では、[DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) オブジェクトを作成する [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) メソッドを呼び出すことで、配布リストを作成します。 その後、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを作成し、[GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) メソッドを呼び出して、既定の [連絡先] フォルダー内で [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) プロパティの値が "Top Custome" になっていて [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) プロパティの値が空でない連絡先をすべて検索します。 すべての連絡先を特定した後で、**Email1Address** の名前を列として **Table** に追加します。 その後、CreateDistributionList では、[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトから [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) メソッドを使用して [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトを作成します。 最後に、CreateDistributionList では "Top Customers" 配布リストをユーザーに表示します。

> [!NOTE] 
> [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) オブジェクトの [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) メソッドには、解決済みの **Recipient** オブジェクトをパラメーターとして渡す必要があります。 **Recipient** オブジェクトを解決するには、[Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) メソッドを使用します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a>関連項目

- [Exchange ユーザー](exchange-users.md)

