---
title: SQLState プロパティ (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6fb45342a56a003856192a353270778b44654de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872180"
---
# <a name="sqlstate-property-ado"></a>SQLState プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

特定の [Error](error-object-ado.md) オブジェクトの SQL 状態を示します。

## <a name="return-value"></a>戻り値

ANSI SQL 標準に準拠し、エラー コードを示す 5 文字の文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

SQL ステートメントの処理中にエラーが発生した場合に、プロバイダーが返す 5 文字のエラー コードを取得するには **SQLState** プロパティを使用します。たとえば、Microsoft OLE DB Provider for ODBC を Microsoft SQL Server データベースと共に使用する場合、ODBC に固有のエラー、または Microsoft SQL Server に起因するエラーに基づいて、ODBC から SQL 状態のエラー コードが生成された後、ODBC エラーにマップされます。これらのエラー コードは ANSI SQL 標準で規定されていますが、実装方法はデータ ソースによって異なる場合があります。

