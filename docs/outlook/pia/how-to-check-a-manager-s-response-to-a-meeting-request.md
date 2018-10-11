---
title: 会議出席依頼に対する上司からの返信を確認する
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 14d78a88a0df514bca6782a84bd2c030fc140093
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406352"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a><span data-ttu-id="5772b-102">会議出席依頼に対する上司からの返信を確認する</span><span class="sxs-lookup"><span data-stu-id="5772b-102">Check a manager's response to a meeting request</span></span>

<span data-ttu-id="5772b-103">この例では、[GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドおよび [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを使用して、会議出席依頼に対する現在のユーザーの上司からの返信の状態を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5772b-103">This example illustrates how to use the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="5772b-104">例</span><span class="sxs-lookup"><span data-stu-id="5772b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5772b-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="5772b-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="5772b-106">ある受信者が会議出席依頼を承諾したか辞退したかを確認するには、[AppointmentItem](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) オブジェクトに関連付けられている [Recipients](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) コレクションから [Recipient](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) オブジェクトの [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5772b-106">To determine whether a given recipient has accepted or declined a requested meeting, use the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object from the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection associated with the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="5772b-107">次のコード サンプルの CheckManagerResponseStatus は、パラメーターとして **AppointmentItem** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="5772b-107">In the following code example,   takes in an AppointmentItem object as a parameter.</span></span> <span data-ttu-id="5772b-108">CheckManagerResponseStatus では、現在のユーザーの **GetExchangeUser** メソッドを呼び出して [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="5772b-108"> gets the ExchangeUser object by calling the GetExchangeUser method on the current user.</span></span> <span data-ttu-id="5772b-109">次に、CheckManagerResponseStatus は **GetExchangeUserManager** メソッドを呼び出して、現在のユーザーの上司に関連付けられている **ExchangeUser** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="5772b-109"> then gets the ExchangeUser object that is associated with the current user's manager by calling the GetExchangeUserManager method.</span></span> <span data-ttu-id="5772b-110">[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) メソッドを使用して、**AppointmentItem** に関連付けられている **Recipient** オブジェクトが、ユーザーの上司を表す **ExchangeUser** オブジェクトと同一であるかどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="5772b-110">By using the [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object, the example then checks whether the **Recipient** object associated with the **AppointmentItem** object is the same as the **ExchangeUser** object that represents the user's manager.</span></span> <span data-ttu-id="5772b-111">**CompareEntryIDs** が **true** を返す場合は、ユーザーの上司が **Recipients** コレクション内に存在し、CheckManagerResponseStatus は上司の **MeetingResponseStatus** を返します。</span><span class="sxs-lookup"><span data-stu-id="5772b-111">If CompareEntryIDs returns true, the user's manager is found in the Recipients collection, and   returns the manager's MeetingResponseStatus.</span></span> <span data-ttu-id="5772b-112">**CompareEntryIDs** が **false** を返す場合、CheckManagerResponseStatus は null 参照を返します。</span><span class="sxs-lookup"><span data-stu-id="5772b-112">If CompareEntryIDs returns false,   returns a null reference.</span></span>

<span data-ttu-id="5772b-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5772b-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="5772b-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5772b-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="5772b-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5772b-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5772b-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="5772b-116">See also</span></span>

- [<span data-ttu-id="5772b-117">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="5772b-117">Exchange Users</span></span>](exchange-users.md)

