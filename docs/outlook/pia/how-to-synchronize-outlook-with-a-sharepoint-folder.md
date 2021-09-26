---
title: Outlook と SharePoint のフォルダーを同期させる
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 000743f394db3eeaf6d6b9d1d3eb98506d0d348b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583087"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a>Outlook と SharePoint のフォルダーを同期させる

この例では、プログラムで Outlook と SharePoint フォルダーを接続して、フォルダーの内容を同期させる方法を説明します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Outlook では、予定表、連絡先リスト、タスク リスト、ディスカッション掲示板、SharePoint フォルダーにドキュメント ライブラリを同期することができます。 同期を行う際に指定された URL に基づいて、Outlook は SharePoint フォルダーと同じベース タイプのフォルダーを新規に作成します。 たとえば、SharePoint の予定表フォルダーと同期させると、Outlook 内に新しい予定表フォルダーが作成されます。 SharePoint と同期されるフォルダーは、ユーザーのメールボックスの外にある固有の Outlook 個人用フォルダー (.pst) ファイルに保存されます。 [OpenSharedFolder (文字列、オブジェクト、オブジェクト、オブジェクト)](https://msdn.microsoft.com/library/bb610157\(v=office.15\))メソッドは[名前空間](https://msdn.microsoft.com/library/bb645857\(v=office.15\))オブジェクトのを使用して、SharePoint フォルダーと接続することができます。 なお、stssync:// URL を使用して、SharePoint フォルダーを開くために Outlook で必要とされる SharePoint サーバーの詳細、フォルダー パス、その他の情報を提供する必要があります。

プログラムで SharePoint フォルダーと接続するときは、共有関係を作成するために使用する適切な URL を決定する必要があります。 フォルダーの SharePoint ユーザー インターフェイスに stssync:// URL は明記されていないため、手動で移動先フォルダーを Outlook にリンクします。 その後、次のコード例で、最初のプロシージャである DisplaySharePointUrl を使用して正しい URL を取得します。 DisplaySharePointUrl は、[表](https://msdn.microsoft.com/library/bb652856\(v=office.15\))オブジェクトを使用して、アクティブなエクスプローラー ウィンドウの現在のフォルダー内から共有バインディング情報を探します。 1 つ以上のバインド コンテキストが検出されると、使用可能なすべての共有コンテキストの URL が表示されます。

共有のリレーションシップを作成する適切な URL が手に入りました。 Outlook の新しい SharePoint フォルダーを同期させるには、URL をコピーして、2 番目のプロシージャである AddSpsFolder 内の文字列変数 CalendarUrl の代入部分に貼り付けます。 AddSpsFolder は、Outlook の新しい SharePoint フォルダーの同期を自動化するために、**NameSpace.OpenSharedFolder** メソッドを `stssync://`URL (今回は、DisplaySharePointUrl プロシージャによって作られた URL) で使用します。 AddSpsFolderalso は、"例 SPS カレンダー" というカスタム フォルダーを提供し、このフォルダーで既定の Time to Live (TTL) を使うよう Outlook に指示します。 SharePoint フォルダーは、アイテムの添付ファイルを常にダウンロードするため、ここで指定する必要はありません。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [グループ共有](group-sharing.md)

