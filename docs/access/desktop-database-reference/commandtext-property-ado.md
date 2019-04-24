---
title: CommandText プロパティ (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296137"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="e3f8b-102">CommandText プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e3f8b-102">CommandText property (ADO)</span></span>


<span data-ttu-id="e3f8b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3f8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3f8b-104">プロバイダーに対して発行するコマンド文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e3f8b-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="e3f8b-105">Settings and return values</span></span>

<span data-ttu-id="e3f8b-p101">SQL ステートメント、テーブル名、相対 URL、またはストアド プロシージャの呼び出しなど、プロバイダーのコマンドを含む文字列型 ( **String** ) の値を設定または取得します。既定値は "" (長さ 0 の文字列) です。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f8b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e3f8b-108">Remarks</span></span>

<span data-ttu-id="e3f8b-p102">**Command** オブジェクトで表されるコマンド テキストを設定または取得するには、 [CommandText](command-object-ado.md) プロパティを使用します。通常は SQL ステートメントを使いますが、ストアド プロシージャの呼び出しなど、プロバイダーが認識する、他の種類のコマンド ステートメントでもかまいません。SQL ステートメントは、特定の文法またはプロバイダーのクエリ プロセッサがサポートするバージョンである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="e3f8b-112">[Command](prepared-property-ado.md) オブジェクトの **Prepared** プロパティが **True** に設定されていて、 **CommandText** プロパティを設定するときに開いていた接続に **Command** オブジェクトがバインドされている場合、 [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッドまたは **Open** メソッドを呼び出すと、クエリ (つまり、プロバイダーが保存するコンパイルされたクエリ) が準備されます。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>

<span data-ttu-id="e3f8b-p103">[CommandType](commandtype-property-ado.md) プロパティの設定値によっては、 **CommandText** プロパティが変更される場合があります。 **CommandText** プロパティはいつでも読み出すことができ、ADO がコマンド実行中に使う実際のコマンド テキストの参照も可能です。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="e3f8b-p104">ファイルやディレクトリなどのリソースを指定する相対 URL を設定したり取得したりするには、 **CommandText** プロパティを使います。リソースは、絶対 URL で明示的に指定された位置や、開かれた [Connection](connection-object-ado.md) オブジェクトで暗黙的に指定された位置に対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <span data-ttu-id="e3f8b-117">[!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-117">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="e3f8b-118">詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3f8b-118">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


