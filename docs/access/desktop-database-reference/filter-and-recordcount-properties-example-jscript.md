---
title: Filter プロパティと RecordCount プロパティの使用例 (JScript)
TOCTitle: Filter and RecordCount properties example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3973105b346c5eb8d8b78fa9eb7f941160258d8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581204"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a>Filter プロパティと RecordCount プロパティの使用例 (JScript)


**適用先**: Access 2013、Office 2013

この例では、Northwind データベースの Companies テーブルの **Recordset** を開き、 [Filter](filter-property-ado.md) プロパティを使って、表示されるレコードを、CompanyName フィールドが文字 D で始まるレコードに制限します。次のコードをコピーし、メモ帳またはその他のテキスト エディターに貼り付けて **FilterJS.asp** という名前で保存してください。

