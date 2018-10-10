---
title: NativeError プロパティ (ADO)
TOCTitle: NativeError Property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98d9695e29df63371b5ee375f864e7b1d4961ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479598"
---
# <a name="nativeerror-property-ado"></a>NativeError プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

指定された [Error](error-object-ado.md) オブジェクトでプロバイダー固有のエラー コードを示します。

## <a name="return-value"></a>戻り値

エラー コードを示す長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**NativeError** プロパティは、特定の **Error** オブジェクトの、データベース固有のエラー情報を取得するために使用します。たとえば、Microsoft ODBC Provider for OLE DB と Microsoft SQL Server データベースを使う場合、SQL Server から送信されたネイティブ エラー コードは、ODBC と ODBC Provider を経由して ADO の **NativeError** プロパティに渡されます。

