---
title: RSS フィードを購読する
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 30370e54e25cad6bc4f138f9d8cc0c8a156b8428
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405827"
---
# <a name="subscribe-to-an-rss-feed"></a><span data-ttu-id="35228-102">RSS フィードを購読する</span><span class="sxs-lookup"><span data-stu-id="35228-102">Subscribe to an RSS feed</span></span>

<span data-ttu-id="35228-103">この例では、[OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) メソッドを使用して RSS フィードを購読する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="35228-103">This example shows how to subscribe to an RSS feed by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="35228-104">例</span><span class="sxs-lookup"><span data-stu-id="35228-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="35228-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="35228-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="35228-p101">Outlook オブジェクト モデルでは、インターネット予定表、RSS フィード、Microsoft SharePoint のリストとドキュメント ライブラリからのデータなどの共有データへのアクセスがサポートされています。このような共有データのソースへ接続して、共有リソースを継続的にポーリングする同期コンテキストをセットアップできます。Outlook オブジェクト モデルには、特定の種類の共有フォルダーを対象にダウンロードと同期を行うために、[NameSpace](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) オブジェクトの [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="35228-p101">The Outlook object model supports providing access to shared data, such as Internet calendars, RSS feeds, and data from Microsoft SharePoint lists and document libraries. It enables connecting to these shared sources of data and setting up the synchronization contexts to continue to poll those shared resources. The Outlook object model provides the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to download and synchronize with a particular type of shared folder.</span></span>

<span data-ttu-id="35228-p102">以下の例の AddRssFeed では、"Example RSS Feed" という名前の新しい RSS フィードを購読するために、その RSS フィードを参照する URL を指定して **OpenSharedFolder** メソッドを呼び出します。**OpenSharedFolder** メソッドの最後の 2 つのパラメーターに **true** を設定して、添付ファイルをダウンロードすること、および RSS フィードで指定されている更新間隔を Outlook で使用することを示します。</span><span class="sxs-lookup"><span data-stu-id="35228-p102">In the following example, AddRssFeed subscribes to a new RSS feed named “Example RSS Feed” by calling the **OpenSharedFolder** method with a URL that refers to the new RSS feed. The last two parameters of **OpenSharedFolder** method are set to **true** to indicate that attachments should be downloaded, and Outlook should use the refresh ratio provided in the RSS feed.</span></span>


> [!NOTE]
> <span data-ttu-id="35228-111">RSS フィードを購読するには、**OpenSharedFolder** メソッドのフォルダー URL に正しいプロトコル ハンドラーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35228-111">You must specify the correct protocol handler for the folder URL in the **OpenSharedFolder** method to subscribe to an RSS feed.</span></span> <span data-ttu-id="35228-112">たとえば、`https://` ではなく `feed://` で始まる URL を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35228-112">For example, you must use a URL that begins with feed:// instead of http://.</span></span> <span data-ttu-id="35228-113">Outlook では、Windows NT LAN Manager (NTLM) 認証を使用できないと認証の必要な RSS フィードを開けず、また、Secure Sockets Layer (SSL) の場所にある RSS フィードは読み込めません。</span><span class="sxs-lookup"><span data-stu-id="35228-113">Outlook cannot open RSS feeds that require authentication unless Windows NT LAN Manager (NTLM) authentication is available, and it cannot load RSS feeds from Secure Sockets Layer (SSL) locations.</span></span>

<span data-ttu-id="35228-114">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="35228-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="35228-115">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35228-115">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="35228-116">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="35228-116">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddRssFeed()
{
    string feedUrl = "feed://example.org/rssfeed.xml";
    Outlook.Folder subscriptionFolder =
        Application.Session.OpenSharedFolder(feedUrl, "Example RSS Feed", true, true) as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(subscriptionFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="35228-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="35228-117">See also</span></span>

- [<span data-ttu-id="35228-118">グループ共有</span><span class="sxs-lookup"><span data-stu-id="35228-118">Group Sharing</span></span>](group-sharing.md)

