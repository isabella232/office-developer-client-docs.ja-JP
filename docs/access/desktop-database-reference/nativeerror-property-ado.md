---
title: NativeError プロパティ (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5ff124266829cc4fe9f13d95c50cb2255eaa4591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577249"
---
# <a name="nativeerror-property-ado"></a>NativeError プロパティ (ADO)


**適用先:** Access 2013、Office 2013

指定された [Error](error-object-ado.md) オブジェクトでプロバイダー固有のエラー コードを示します。

## <a name="return-value"></a>戻り値

エラー コードを示す長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

**NativeError** プロパティは、特定の **Error** オブジェクトの、データベース固有のエラー情報を取得するために使用します。たとえば、Microsoft ODBC Provider for OLE DB と Microsoft SQL Server データベースを使う場合、SQL Server から送信されたネイティブ エラー コードは、ODBC と ODBC Provider を経由して ADO の **NativeError** プロパティに渡されます。

