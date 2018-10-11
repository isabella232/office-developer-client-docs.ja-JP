---
title: 電子名刺のレイアウトを変更する
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0b95621df2e021f52587d5a40d0de43e5505b80c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406436"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a><span data-ttu-id="93e76-102">電子名刺のレイアウトを変更する</span><span class="sxs-lookup"><span data-stu-id="93e76-102">Modify the layout of an electronic business card</span></span>

<span data-ttu-id="93e76-103">この例では、[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) インターフェイスの [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) プロパティを使用して、電子名刺のレイアウトを変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="93e76-103">This example shows how to modify the layout of an Electronic Business Card by using the [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) property of the [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) interface.</span></span>

## <a name="example"></a><span data-ttu-id="93e76-104">例</span><span class="sxs-lookup"><span data-stu-id="93e76-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="93e76-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="93e76-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="93e76-106">電子名刺には、連絡先から特定の情報をキャプチャする連絡先ビューが示されます。</span><span class="sxs-lookup"><span data-stu-id="93e76-106">An Electronic Business Card provides a contact view that captures specific information from that contact.</span></span> <span data-ttu-id="93e76-107">**ContactItem** インターフェイスは、電子名刺に関連する特定のメンバーを提供します。</span><span class="sxs-lookup"><span data-stu-id="93e76-107">The **ContactItem** interface provides specific members that pertain to Electronic Business Cards.</span></span> <span data-ttu-id="93e76-108">そのメンバーとは、**BusinessCardLayoutXml**、[BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\))、[AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\))、[ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\))、[ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\))、[SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\))、および [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)) です。</span><span class="sxs-lookup"><span data-stu-id="93e76-108">These members are **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)) , [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)) , [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)) , [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)) , [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) , and [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)) .</span></span>

<span data-ttu-id="93e76-109">次のコード例では、電子名刺のレイアウトを変更するために、まず、BusinessCardLayoutExample で **ContactItem** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="93e76-109">In the following code example,   modifies the layout of an Electronic Business Card by first obtaining a specified ContactItem object.</span></span> <span data-ttu-id="93e76-110">この例の場合、**ContactItem** は [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) プロパティの値が "Melissa MacBeth" と一致する連絡先です。</span><span class="sxs-lookup"><span data-stu-id="93e76-110">In this case, the **ContactItem** is a contact with the value of the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property equal to "Melissa MacBeth".</span></span> <span data-ttu-id="93e76-111">その次に、BusinessCardLayoutExample で XML ドキュメント クラス [XmlDocument](https://msdn.microsoft.com/ja-JP/library/6kza7w4k) を作成して、このクラスの layout 属性を文字列で取得するために **ContactItem** オブジェクトの **BusinessCardLayoutXML** 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="93e76-111">Next,   creates an XML document class XmlDocument , and then gets the layout attribute of this class in a string by using the BusinessCardLayoutXML value for the ContactItem object.</span></span> <span data-ttu-id="93e76-112">その後で、カードのレイアウトを左揃えから右揃えに変更します。</span><span class="sxs-lookup"><span data-stu-id="93e76-112">The card layout is then changed from left-aligned to right-aligned.</span></span>

<span data-ttu-id="93e76-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93e76-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="93e76-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93e76-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="93e76-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="93e76-115">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="93e76-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="93e76-116">See also</span></span>

- [<span data-ttu-id="93e76-117">電子名刺</span><span class="sxs-lookup"><span data-stu-id="93e76-117">Electronic Business Cards</span></span>](electronic-business-cards.md)

