---
title: フォルダーの既定のメッセージ クラスを取得する
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 031b7736ed397b9218ea677442f80595da2aa919
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542563"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="7bfad-102">フォルダーの既定のメッセージ クラスを取得する</span><span class="sxs-lookup"><span data-stu-id="7bfad-102">Get the default message class of a folder</span></span>

<span data-ttu-id="7bfad-103">この例では、[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) プロパティを使用してフォルダーの既定のメッセージ クラスを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7bfad-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="7bfad-104">例</span><span class="sxs-lookup"><span data-stu-id="7bfad-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7bfad-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="7bfad-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="7bfad-106">フォルダーの既定のメッセージ クラスを取得するには、[MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトの **DefaultMessageClass** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7bfad-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="7bfad-107">たとえば、[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトの **DefaultMessageClass** が IPM.Contact であれば、Contact フォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="7bfad-107">For example, a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that has a **DefaultMessageClass** of IPM.Contact means that it represents a Contact folder.</span></span> <span data-ttu-id="7bfad-108">しかし、フォルダーの既定のフォームがカスタム フォームまたは代替フォームの場合は、 [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを使用して既定のフォームのメッセージ クラスを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bfad-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="7bfad-109">**DefaultMessageClass** プロパティはフォルダーの既定のフォームのメッセージ クラスを返しません。</span><span class="sxs-lookup"><span data-stu-id="7bfad-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="7bfad-110">次のコード例では、GetDefaultMessageClass プロシージャが **PropertyAccessor** を使用してフォルダーの既定のフォームを決定します。</span><span class="sxs-lookup"><span data-stu-id="7bfad-110">In the following code example, the GetDefaultMessageClass procedure uses the **PropertyAccessor** to determine the default form of a folder.</span></span> <span data-ttu-id="7bfad-111">フォルダー プロパティ **PR \_ DEF POST \_ \_ MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\))が見つからない場合、Outlookエラーが発生する場合は **、try..。catch** ブロックは **、Folder の DefaultMessageClass** プロパティを返 **します**。</span><span class="sxs-lookup"><span data-stu-id="7bfad-111">If the folder property **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) is not found and Outlook raises an error, the **try…catch** block returns the **DefaultMessageClass** property for the **Folder**.</span></span>

<span data-ttu-id="7bfad-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7bfad-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7bfad-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bfad-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7bfad-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bfad-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7bfad-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bfad-115">See also</span></span>

- [<span data-ttu-id="7bfad-116">フォルダー</span><span class="sxs-lookup"><span data-stu-id="7bfad-116">Folders</span></span>](folders.md)

