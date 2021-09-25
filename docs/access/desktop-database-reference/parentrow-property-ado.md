---
title: ParentRow プロパティ (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 372ae0fb41887a3b4bf7203070530d9e00215ccb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568671"
---
# <a name="parentrow-property-ado"></a>ParentRow プロパティ (ADO)

**適用先:** Access 2013、Office 2013

OLE DB **Row** オブジェクトのコンテナーを **ADORecordConstruction** オブジェクトに設定し、行の親が ADO **Record** オブジェクトに変換されるようにします。

値の設定のみ可能です。

## <a name="syntax"></a>構文

HRESULT は \_ ParentRow( in \[ \] IUnknown \* pParent) を置く。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*pParent* |行のコンテナー。|

## <a name="return-values"></a>戻り値

このプロパティ メソッドは、標準の HRESULT 値 (S \_ OK、E FAIL など) を返 \_ します。

## <a name="applies-to"></a>適用対象

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

