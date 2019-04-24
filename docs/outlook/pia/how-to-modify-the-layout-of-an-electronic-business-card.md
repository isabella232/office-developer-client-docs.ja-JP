---
title: 電子名刺のレイアウトを変更する
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f85324b31ae865c69e2c40806d9654a0b443f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320182"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>電子名刺のレイアウトを変更する

この例では、[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) インターフェイスの [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) プロパティを使用して、電子名刺のレイアウトを変更する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

電子名刺には、連絡先から特定の情報をキャプチャする連絡先ビューが示されます。 **ContactItem** インターフェイスは、電子名刺に関連する特定のメンバーを提供します。 そのメンバーとは、**BusinessCardLayoutXml**、[BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\))、[AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\))、[ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\))、[ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\))、[SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\))、および [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)) です。

次のコード例では、電子名刺のレイアウトを変更するために、まず、BusinessCardLayoutExample で **ContactItem** オブジェクトを取得します。 この例の場合、**ContactItem** は [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) プロパティの値が "Melissa MacBeth" と一致する連絡先です。 その次に、BusinessCardLayoutExample で XML ドキュメント クラス [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k) を作成して、このクラスの layout 属性を文字列で取得するために **ContactItem** オブジェクトの **BusinessCardLayoutXML** 値を使用します。 その後で、カードのレイアウトを左揃えから右揃えに変更します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [電子名刺](electronic-business-cards.md)

