---
title: CommandText プロパティ (ADO)
TOCTitle: CommandText Property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9000f069c7669872c686c013520f886d16e3619b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476256"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="8c2e7-102">CommandText プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8c2e7-102">CommandText Property (ADO)</span></span>


<span data-ttu-id="8c2e7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c2e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8c2e7-104">プロバイダーに対して発行するコマンド文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8c2e7-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="8c2e7-105">Settings and Return Values</span></span>

<span data-ttu-id="8c2e7-p101">SQL ステートメント、テーブル名、相対 URL、またはストアド プロシージャの呼び出しなど、プロバイダーのコマンドを含む文字列型 ( **String** ) の値を設定または取得します。既定値は "" (長さ 0 の文字列) です。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c2e7-108">解説</span><span class="sxs-lookup"><span data-stu-id="8c2e7-108">Remarks</span></span>

<span data-ttu-id="8c2e7-p102">**Command** オブジェクトで表されるコマンド テキストを設定または取得するには、 [CommandText](command-object-ado.md) プロパティを使用します。通常は SQL ステートメントを使いますが、ストアド プロシージャの呼び出しなど、プロバイダーが認識する、他の種類のコマンド ステートメントでもかまいません。SQL ステートメントは、特定の文法またはプロバイダーのクエリ プロセッサがサポートするバージョンである必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="8c2e7-112">[Command](prepared-property-ado.md) オブジェクトの **Prepared** プロパティが **True** に設定されていて、 **CommandText** プロパティを設定するときに開いていた接続に **Command** オブジェクトがバインドされている場合、 [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) メソッドまたは **Open** メソッドを呼び出すと、クエリ (つまり、プロバイダーが保存するコンパイルされたクエリ) が準備されます。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) or **Open** methods.</span></span>

<span data-ttu-id="8c2e7-p103">[CommandType](commandtype-property-ado.md) プロパティの設定値によっては、 **CommandText** プロパティが変更される場合があります。 **CommandText** プロパティはいつでも読み出すことができ、ADO がコマンド実行中に使う実際のコマンド テキストの参照も可能です。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="8c2e7-p104">ファイルやディレクトリなどのリソースを指定する相対 URL を設定したり取得したりするには、 **CommandText** プロパティを使います。リソースは、絶対 URL で明示的に指定された位置や、開かれた [Connection](connection-object-ado.md) オブジェクトで暗黙的に指定された位置に対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8c2e7-p105">[!メモ] http スキームを使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c2e7-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


