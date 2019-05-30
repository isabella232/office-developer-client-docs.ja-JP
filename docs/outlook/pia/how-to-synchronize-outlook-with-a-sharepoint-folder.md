---
title: Outlook と SharePoint のフォルダーを同期させる
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ab8da62d75b5714967c3fbdc0d0f985370e617aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540638"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a><span data-ttu-id="d160d-102">Outlook と SharePoint のフォルダーを同期させる</span><span class="sxs-lookup"><span data-stu-id="d160d-102">Synchronize Outlook with a SharePoint folder</span></span>

<span data-ttu-id="d160d-103">この例では、プログラムで Outlook と SharePoint フォルダーを接続して、フォルダーの内容を同期させる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d160d-103">This example shows how to programmatically connect Outlook with a SharePoint folder and to synchronize the folder contents.</span></span>

## <a name="example"></a><span data-ttu-id="d160d-104">例</span><span class="sxs-lookup"><span data-stu-id="d160d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d160d-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="d160d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d160d-106">Outlook では、予定表、連絡先リスト、タスク リスト、ディスカッション掲示板、SharePoint フォルダーにドキュメント ライブラリを同期することができます。</span><span class="sxs-lookup"><span data-stu-id="d160d-106">In Outlook, you can synchronize calendars, contact lists, task lists, discussion boards, and document libraries to SharePoint folders.</span></span> <span data-ttu-id="d160d-107">同期を行う際に指定された URL に基づいて、Outlook は SharePoint フォルダーと同じベース タイプのフォルダーを新規に作成します。</span><span class="sxs-lookup"><span data-stu-id="d160d-107">Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder.</span></span> <span data-ttu-id="d160d-108">たとえば、SharePoint の予定表フォルダーと同期させると、Outlook 内に新しい予定表フォルダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d160d-108">For example, synchronizing to a SharePoint calendar folder will create a new calendar folder in Outlook.</span></span> <span data-ttu-id="d160d-109">SharePoint と同期されるフォルダーは、ユーザーのメールボックスの外にある固有の Outlook 個人用フォルダー (.pst) ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="d160d-109">SharePoint synchronization folders are stored in their own Outlook Personal Folders (.pst) file outside of the user’s mailbox.</span></span> <span data-ttu-id="d160d-110">[OpenSharedFolder (文字列、オブジェクト、オブジェクト、オブジェクト)](https://msdn.microsoft.com/library/bb610157\(v=office.15\))メソッドは[名前空間](https://msdn.microsoft.com/library/bb645857\(v=office.15\))オブジェクトのを使用して、SharePoint フォルダーと接続することができます。</span><span class="sxs-lookup"><span data-stu-id="d160d-110">You can connect to a SharePoint folder by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="d160d-111">なお、stssync:// URL を使用して、SharePoint フォルダーを開くために Outlook で必要とされる SharePoint サーバーの詳細、フォルダー パス、その他の情報を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d160d-111">Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.</span></span>

<span data-ttu-id="d160d-112">プログラムで SharePoint フォルダーと接続するときは、共有関係を作成するために使用する適切な URL を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d160d-112">When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship.</span></span> <span data-ttu-id="d160d-113">フォルダーの SharePoint ユーザー インターフェイスに stssync:// URL は明記されていないため、手動で移動先フォルダーを Outlook にリンクします。</span><span class="sxs-lookup"><span data-stu-id="d160d-113">Because the stssync:// URL is not provided in the SharePoint user interface for the folder, manually link the destination folder into Outlook.</span></span> <span data-ttu-id="d160d-114">その後、次のコード例で、最初のプロシージャである DisplaySharePointUrl を使用して正しい URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="d160d-114">Then use the first procedure, DisplaySharePointUrl, in the following code example, to get the correct URL.</span></span> <span data-ttu-id="d160d-115">DisplaySharePointUrl は、[表](https://msdn.microsoft.com/library/bb652856\(v=office.15\))オブジェクトを使用して、アクティブなエクスプローラー ウィンドウの現在のフォルダー内から共有バインディング情報を探します。</span><span class="sxs-lookup"><span data-stu-id="d160d-115">DisplaySharePointUrl uses the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to look for the sharing binding information in the current folder for the active explorer window.</span></span> <span data-ttu-id="d160d-116">1 つ以上のバインド コンテキストが検出されると、使用可能なすべての共有コンテキストの URL が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d160d-116">If one or more binding contexts are found, the URLs for all available sharing contexts will be displayed.</span></span>

<span data-ttu-id="d160d-117">共有のリレーションシップを作成する適切な URL が手に入りました。</span><span class="sxs-lookup"><span data-stu-id="d160d-117">Now you have the proper URL to create the sharing relationship.</span></span> <span data-ttu-id="d160d-118">Outlook の新しい SharePoint フォルダーを同期させるには、URL をコピーして、2 番目のプロシージャである AddSpsFolder 内の文字列変数 CalendarUrl の代入部分に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d160d-118">To synchronize the new SharePoint folder in Outlook, copy and paste the URL to the assignment of the string variable calendarUrl in the second procedure, AddSpsFolder.</span></span> <span data-ttu-id="d160d-119">AddSpsFolder は、Outlook の新しい SharePoint フォルダーの同期を自動化するために、**NameSpace.OpenSharedFolder** メソッドを `stssync://`URL (今回は、DisplaySharePointUrl プロシージャによって作られた URL) で使用します。</span><span class="sxs-lookup"><span data-stu-id="d160d-119">AddSpsFolder automates the synchronization of the new SharePoint folder in Outlook by using the **NameSpace.OpenSharedFolder** method with a `stssync://` URL (in this case, the URL produced by the DisplaySharePointUrl procedure).</span></span> <span data-ttu-id="d160d-120">AddSpsFolderalso は、"例 SPS カレンダー" というカスタム フォルダーを提供し、このフォルダーで既定の Time to Live (TTL) を使うよう Outlook に指示します。</span><span class="sxs-lookup"><span data-stu-id="d160d-120">AddSpsFolderalso provides a custom folder name, “Example SPS Calendar”, and specifies Outlook to use the default Time to Live (TTL) for the folder.</span></span> <span data-ttu-id="d160d-121">SharePoint フォルダーは、アイテムの添付ファイルを常にダウンロードするため、ここで指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d160d-121">SharePoint folders always download item attachments, so you do not have to specify that here.</span></span>

<span data-ttu-id="d160d-122">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d160d-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d160d-123">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d160d-123">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d160d-124">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d160d-124">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "http://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="d160d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d160d-125">See also</span></span>

- [<span data-ttu-id="d160d-126">グループ共有</span><span class="sxs-lookup"><span data-stu-id="d160d-126">Group sharing</span></span>](group-sharing.md)

