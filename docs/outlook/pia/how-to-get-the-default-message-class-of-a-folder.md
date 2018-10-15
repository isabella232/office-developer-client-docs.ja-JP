---
title: フォルダーの既定のメッセージ クラスを取得する
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c03e0737a3dd2e74f39d90ffbac31bb134d16348
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407220"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="ae388-102">フォルダーの既定のメッセージ クラスを取得する</span><span class="sxs-lookup"><span data-stu-id="ae388-102">Get the default message class of a folder</span></span>

<span data-ttu-id="ae388-103">この例では、[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) プロパティを使用してフォルダーの既定のメッセージ クラスを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ae388-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="ae388-104">例</span><span class="sxs-lookup"><span data-stu-id="ae388-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ae388-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="ae388-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="ae388-106">フォルダーの既定のメッセージ クラスを取得するには、[MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトの **DefaultMessageClass** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae388-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="ae388-107">たとえば、[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトの **DefaultMessageClass** が IPM.Contact であれば、Contact フォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="ae388-107">For example, a Folder object that has a DefaultMessageClass of   means that it represents a Contact folder.</span></span> <span data-ttu-id="ae388-108">しかし、フォルダーの既定のフォームがカスタム フォームまたは代替フォームの場合は、 [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを使用して既定のフォームのメッセージ クラスを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae388-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="ae388-109">**DefaultMessageClass** プロパティはフォルダーの既定のフォームのメッセージ クラスを返しません。</span><span class="sxs-lookup"><span data-stu-id="ae388-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="ae388-110">次のコード例では、GetDefaultMessageClass プロシージャが **PropertyAccessor** を使用してフォルダーの既定のフォームを決定します。</span><span class="sxs-lookup"><span data-stu-id="ae388-110">In the following code example, the   procedure uses the PropertyAccessor to determine the default form of a folder.</span></span> <span data-ttu-id="ae388-111">フォルダーのプロパティ **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) が見つからず、Outlook でエラーが発生すると、**try…catch** ブロックから **Folder** の **DefaultMessageClass** プロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="ae388-111">If the folder property PR_DEF_POST_MSGCLASS (PidTagDefaultPostMessageClass) is not found and Outlook raises an error, the try…catch block returns the DefaultMessageClass property for the Folder.</span></span>

<span data-ttu-id="ae388-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae388-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ae388-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae388-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ae388-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ae388-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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
            @"https://schemas.microsoft.com/mapi/proptag/0x36E5001E";
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

## <a name="see-also"></a><span data-ttu-id="ae388-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae388-115">See also</span></span>

- [<span data-ttu-id="ae388-116">フォルダー</span><span class="sxs-lookup"><span data-stu-id="ae388-116">Folders</span></span>](folders.md)

