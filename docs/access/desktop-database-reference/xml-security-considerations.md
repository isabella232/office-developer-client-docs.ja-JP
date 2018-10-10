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
# <a name="xml-security-considerations"></a>XML のセキュリティに関する考慮事項


**適用されます**Access 2013 |。Office 2013

## <a name="xml-security-considerations"></a>XML のセキュリティに関する考慮事項

**Recordset** オブジェクトの ADO **Save** メソッドおよび ADO **Open** メソッドは、Internet Explorer で実行する操作として安全ではないと考えられています。そのため、ブラウザーでホストされるアプリケーションまたはコントロール内で実行されるスクリプト コードでこれらのメソッドを使用すると、ブラウザーのセキュリティ構成がスクリプト コードの動作に影響します。

Internet Explorer 5 は、このような操作に対して、インターネット ゾーンでは既定でセキュリティ制限をかけています。その構成では、 **Recordset** は、クライアントのローカル ファイル システムにアクセスしたり、ページがダウンロードされたサーバーのドメインの範囲外にあるデータ ソースにアクセスしたりすることはできません。特に、ブラウザー ホスト内で実行している場合、 **Recordset** をファイルに保存できるのは、ページがダウンロードされたサーバーと同じサーバーにファイルがある場合のみです。同様に、ファイルから **Recordset** を読み込んで開くことができるのは、ページがダウンロードされたサーバーと同じサーバーにファイルがある場合のみです。

Internet Explorer のセキュリティの詳細については、Microsoft Internet Explorer での ADO および RDS の セキュリティに関する技術記事を参照してください。

