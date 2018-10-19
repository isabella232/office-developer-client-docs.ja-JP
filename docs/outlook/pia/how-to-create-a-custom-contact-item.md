---
title: カスタムの連絡先アイテムを作成する
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 189be01e6e690ad1db3d58d58837ab418b4c2e74
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407346"
---
# <a name="create-a-custom-contact-item"></a>カスタムの連絡先アイテムを作成する

この例では、カスタムの連絡先アイテムを作成し、定義済みのプロパティとユーザー定義プロパティの両方を設定する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) オブジェクトは連絡先フォルダー内の連絡先を表します。また、[FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) や [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)) など、100 個以上の組み込みプロパティを持っています。 これらの組み込みプロパティでは不十分な場合もあります。その場合はカスタム プロパティを追加する必要があります。カスタム プロパティは、[UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) コレクションを使用すると追加できます。

次のコード例では、CreateCustomItem でカスタム **ContactItem** オブジェクトを作成し、"Shoe Store" という名前を付け、[Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) メソッドを呼び出して、"Shoe Store" という名前のフォルダーに追加します。 まず CreateCustomItem は、[GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) メソッドを使用して "Shoe Store" フォルダーを取得します。 "Shoe Store" フォルダーは既定の連絡先フォルダーのサブフォルダーです。 次に、CreateCustomItem は **FirstName** プロパティと **LastName** プロパティを設定し、**UserProperties** コレクションを使用してユーザー定義プロパティ ("Shoe Size") を作成します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a>関連項目

- [連絡先](contacts.md)

