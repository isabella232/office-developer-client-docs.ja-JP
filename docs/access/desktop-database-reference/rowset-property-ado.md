---
title: Rowset プロパティ (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ad31c4b34f4e94329907264e8ed29eddc08dbecb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615012"
---
# <a name="rowset-property-ado"></a>Rowset プロパティ (ADO)

**適用先**: Access 2013、Office 2013

**ADORecordsetConstruction** オブジェクトの OLE DB **Rowset** オブジェクトを取得または設定します。 Put \_ **Rowset** を使用すると、行セットは ADO Recordset オブジェクトに変換されます。

値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get \_ Rowset( \[ out, retval \] IUnknown \* \* ppRowset);

HRESULT は \_ 、行セット \[ \] (IUnknown \* pRowset) を入れる。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ppRowset* |OLE DB **Rowset** オブジェクトを指すポインター。|
|*PRowset* |OLE DB **Rowset** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティ メソッドは、標準の HRESULT 値 (S \_ OK、E FAIL など) を返 \_ します。

## <a name="applies-to"></a>適用対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

