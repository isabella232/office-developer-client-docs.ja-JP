---
title: SQLState プロパティ (ADO)
TOCTitle: SQLState Property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aead95e4276d61d69ae6ba5a86974cbe630f9043
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477867"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="c26b4-102">SQLState プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="c26b4-102">SQLState Property (ADO)</span></span>


<span data-ttu-id="c26b4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c26b4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c26b4-104">特定の [Error](error-object-ado.md) オブジェクトの SQL 状態を示します。</span><span class="sxs-lookup"><span data-stu-id="c26b4-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="c26b4-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="c26b4-105">Return Value</span></span>

<span data-ttu-id="c26b4-106">ANSI SQL 標準に準拠し、エラー コードを示す 5 文字の文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="c26b4-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c26b4-107">解説</span><span class="sxs-lookup"><span data-stu-id="c26b4-107">Remarks</span></span>

<span data-ttu-id="c26b4-p101">SQL ステートメントの処理中にエラーが発生した場合に、プロバイダーが返す 5 文字のエラー コードを取得するには **SQLState** プロパティを使用します。たとえば、Microsoft OLE DB Provider for ODBC を Microsoft SQL Server データベースと共に使用する場合、ODBC に固有のエラー、または Microsoft SQL Server に起因するエラーに基づいて、ODBC から SQL 状態のエラー コードが生成された後、ODBC エラーにマップされます。これらのエラー コードは ANSI SQL 標準で規定されていますが、実装方法はデータ ソースによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c26b4-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

