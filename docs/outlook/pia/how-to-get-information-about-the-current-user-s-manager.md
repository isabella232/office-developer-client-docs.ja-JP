---
title: 現在のユーザーの上司の情報を取得する
TOCTitle: Get information about the current user's manager
ms:assetid: 3a77fa51-e2e3-4544-849f-4267b1762270
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184603(v=office.15)
ms:contentKeyID: 55119846
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 89da7df4aac29b7d308dd0b0f432d8652c5f0127
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407311"
---
# <a name="get-information-about-the-current-users-manager"></a><span data-ttu-id="a68ef-102">現在のユーザーの上司の情報を取得する</span><span class="sxs-lookup"><span data-stu-id="a68ef-102">Get information about the current user's manager</span></span>

<span data-ttu-id="a68ef-103">この例では、現在のユーザーの上司の情報 (名前、役職、電話番号など) を取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a68ef-103">This example shows how to get information (such as name, job title, and phone numbers) about the current user’s manager.</span></span>

## <a name="example"></a><span data-ttu-id="a68ef-104">例</span><span class="sxs-lookup"><span data-stu-id="a68ef-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a68ef-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="a68ef-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="a68ef-106">次のプロシージャで、GetManagerInfo は [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを呼び出して、組織階層で **ExchangeUser** の上司を表す [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="a68ef-106">In the following procedure,   calls the GetExchangeUserManager() method to obtain an ExchangeUser object that represents the manager of an ExchangeUser in the organizational hierarchy.</span></span> <span data-ttu-id="a68ef-107">このプロシージャは、ログオン ユーザーがオンラインかどうかをテストし、**GetExchangeUserManager** から確実に **ExchangeUser** オブジェクトが返されるようにします。</span><span class="sxs-lookup"><span data-stu-id="a68ef-107">The procedure tests whether the logged-on user is online to ensure that **GetExchangeUserManager** can return an **ExchangeUser** object.</span></span> <span data-ttu-id="a68ef-108">ユーザーがオンラインでない場合、**GetExchangeUserManager** は Null 参照を返します。</span><span class="sxs-lookup"><span data-stu-id="a68ef-108">If the user is not online, **GetExchangeUserManager** will return a null reference.</span></span> <span data-ttu-id="a68ef-109">その後、GetManagerInfo は [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに上司の情報を書き出します。</span><span class="sxs-lookup"><span data-stu-id="a68ef-109"> then writes manager information to the trace listeners of the Listeners collection.</span></span>

<span data-ttu-id="a68ef-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a68ef-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="a68ef-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a68ef-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="a68ef-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a68ef-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerInfo()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + manager.Name);
            sb.AppendLine("STMP address: "
                + manager.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + manager.JobTitle);
            sb.AppendLine("Department: "
                + manager.Department);
            sb.AppendLine("Location: "
                + manager.OfficeLocation);
            sb.AppendLine("Business phone: "
                + manager.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + manager.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a68ef-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="a68ef-113">See also</span></span>

- [<span data-ttu-id="a68ef-114">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="a68ef-114">Exchange Users</span></span>](exchange-users.md)

