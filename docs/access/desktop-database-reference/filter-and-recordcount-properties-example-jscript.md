---
title: Filter プロパティと RecordCount プロパティの使用例 (JScript)
TOCTitle: Filter and RecordCount Properties Example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f6b33ce6824144626a9219fa2d218d90b38ed89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478286"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a>Filter プロパティと RecordCount プロパティの使用例 (JScript)


**適用されます**Access 2013 |。Office 2013

この例では、Northwind データベースの Companies テーブルの **Recordset** を開き、 [Filter](filter-property-ado.md) プロパティを使って、表示されるレコードを、CompanyName フィールドが文字 D で始まるレコードに制限します。次のコードをコピーし、メモ帳またはその他のテキスト エディターに貼り付けて **FilterJS.asp** という名前で保存してください。

