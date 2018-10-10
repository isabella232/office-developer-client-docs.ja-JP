---
title: XML のセキュリティに関する考慮事項
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3120db77ba89aee1036de4d6fa85df73c21d26d9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478868"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="5f8e9-102">XML のセキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="5f8e9-102">XML Security Considerations</span></span>


<span data-ttu-id="5f8e9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f8e9-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="5f8e9-104">XML のセキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="5f8e9-104">XML Security Considerations</span></span>

<span data-ttu-id="5f8e9-p101">**Recordset** オブジェクトの ADO **Save** メソッドおよび ADO **Open** メソッドは、Internet Explorer で実行する操作として安全ではないと考えられています。そのため、ブラウザーでホストされるアプリケーションまたはコントロール内で実行されるスクリプト コードでこれらのメソッドを使用すると、ブラウザーのセキュリティ構成がスクリプト コードの動作に影響します。</span><span class="sxs-lookup"><span data-stu-id="5f8e9-p101">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer. Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="5f8e9-p102">Internet Explorer 5 は、このような操作に対して、インターネット ゾーンでは既定でセキュリティ制限をかけています。その構成では、 **Recordset** は、クライアントのローカル ファイル システムにアクセスしたり、ページがダウンロードされたサーバーのドメインの範囲外にあるデータ ソースにアクセスしたりすることはできません。特に、ブラウザー ホスト内で実行している場合、 **Recordset** をファイルに保存できるのは、ページがダウンロードされたサーバーと同じサーバーにファイルがある場合のみです。同様に、ファイルから **Recordset** を読み込んで開くことができるのは、ページがダウンロードされたサーバーと同じサーバーにファイルがある場合のみです。</span><span class="sxs-lookup"><span data-stu-id="5f8e9-p102">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones. Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded. Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded. Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="5f8e9-111">Internet Explorer のセキュリティの詳細については、Microsoft Internet Explorer での ADO および RDS の セキュリティに関する技術記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f8e9-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>

