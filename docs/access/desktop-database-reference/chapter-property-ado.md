---
title: Chapter プロパティ (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1732e32e784f84ab6b21855f94c5b326420cfe41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618512"
---
# <a name="chapter-property-ado"></a>Chapter プロパティ (ADO)

**適用先**: Access 2013、Office 2013
 
Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object. Put Chapter を **使用して \_ Chapter** オブジェクトを設定すると、行のサブセットが ADO Recordset オブジェクトに **変換** されます。  This sets the current chapter of the **Rowset** object. 値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);

HRESULT は \_ Chapter( を長 \[ い \] lChapter に入れる);

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*plChapter* |チャプターのハンドルへのポインターです。|
|*LChapter* |チャプターのハンドルです。|

## <a name="return-values"></a>戻り値

このプロパティ メソッドは、標準の HRESULT 値 (S \_ OK、E FAIL など) を返 \_ します。

## <a name="applies-to"></a>対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

