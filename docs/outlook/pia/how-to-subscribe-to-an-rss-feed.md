---
title: RSS フィードを購読する
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4f6f2067605208966d095a83137947dd9232b6a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583108"
---
# <a name="subscribe-to-an-rss-feed"></a>RSS フィードを購読する

この例では、[OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) メソッドを使用して RSS フィードを購読する方法を示しています。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Outlook オブジェクト モデルでは、インターネット予定表、RSS フィード、Microsoft SharePoint のリストとドキュメント ライブラリからのデータなどの共有データへのアクセスがサポートされています。このような共有データのソースへ接続して、共有リソースを継続的にポーリングする同期コンテキストをセットアップできます。Outlook オブジェクト モデルには、特定の種類の共有フォルダーを対象にダウンロードと同期を行うために、[NameSpace](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) オブジェクトの [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドが用意されています。

以下の例の AddRssFeed では、"Example RSS Feed" という名前の新しい RSS フィードを購読するために、その RSS フィードを参照する URL を指定して **OpenSharedFolder** メソッドを呼び出します。**OpenSharedFolder** メソッドの最後の 2 つのパラメーターに **true** を設定して、添付ファイルをダウンロードすること、および RSS フィードで指定されている更新間隔を Outlook で使用することを示します。


> [!NOTE]
> RSS フィードを購読するには、**OpenSharedFolder** メソッドのフォルダー URL に正しいプロトコル ハンドラーを指定する必要があります。 たとえば、`https://` ではなく `feed://` で始まる URL を使用する必要があります。 Outlook では、Windows NT LAN Manager (NTLM) 認証を使用できないと認証の必要な RSS フィードを開けず、また、Secure Sockets Layer (SSL) の場所にある RSS フィードは読み込めません。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [グループ共有](group-sharing.md)

