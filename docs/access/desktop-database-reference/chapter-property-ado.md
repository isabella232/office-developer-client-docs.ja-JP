---
title: Chapter プロパティ (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296396"
---
# <a name="chapter-property-ado"></a>Chapter プロパティ (ADO)

**適用先:** Access 2013、Office 2013
 
Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object. **put\_チャプター**を使用して**チャプター**オブジェクトを設定すると、行のサブセットが ADO **Recordset**オブジェクトになります。 This sets the current chapter of the **Rowset** object. 値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_チャプター (\[out, retval\] long\* plchapter);

HRESULT put\_チャプター (\[\]長い lchapter)。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*plchapter* |チャプターのハンドルへのポインターです。|
|*LChapter* |チャプターのハンドルです。|

## <a name="return-values"></a>戻り値

このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。

## <a name="applies-to"></a>対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

