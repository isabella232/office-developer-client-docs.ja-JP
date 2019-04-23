---
title: /エラープロパティ (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288611"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="08de9-102">/エラープロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="08de9-102">NativeError property (ADO)</span></span>


<span data-ttu-id="08de9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="08de9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08de9-104">指定された [Error](error-object-ado.md) オブジェクトでプロバイダー固有のエラー コードを示します。</span><span class="sxs-lookup"><span data-stu-id="08de9-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="08de9-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="08de9-105">Return value</span></span>

<span data-ttu-id="08de9-106">エラー コードを示す長整数型 (**Long**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="08de9-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08de9-107">注釈</span><span class="sxs-lookup"><span data-stu-id="08de9-107">Remarks</span></span>

<span data-ttu-id="08de9-p101">**NativeError** プロパティは、特定の **Error** オブジェクトの、データベース固有のエラー情報を取得するために使用します。たとえば、Microsoft ODBC Provider for OLE DB と Microsoft SQL Server データベースを使う場合、SQL Server から送信されたネイティブ エラー コードは、ODBC と ODBC Provider を経由して ADO の **NativeError** プロパティに渡されます。</span><span class="sxs-lookup"><span data-stu-id="08de9-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

