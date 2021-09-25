---
title: RowPosition プロパティ (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 26ef8dc573e548dbdb2d35d53bd470df63ce17f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615040"
---
# <a name="rowposition-property-ado"></a>RowPosition プロパティ (ADO)

**適用先**: Access 2013、Office 2013

**ADORecordsetConstruction** オブジェクトの OLE DB **RowPosition** オブジェクトを取得または設定します。 Put **\_ RowPosition を使用して RowPosition** オブジェクトを設定すると、結果の **Recordset** オブジェクトは **RowPosition** オブジェクトを使用して現在の行を決定します。

値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);

HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ppRowPos* |OLE DB **RowPosition** オブジェクトを指すポインター。|
|*PRowPos* |OLE DB **RowPosition** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティ メソッドは、標準の HRESULT 値 (S \_ OK、E FAIL など) を返 \_ します。

## <a name="remarks"></a>注釈

このプロパティを設定したときに、**RowPosition** オブジェクトの **Rowset** オブジェクトと **Recordset** オブジェクトの **Rowset** オブジェクトが異なる場合、前者が後者よりも優先されます。同様の動作が **RowPosition** の現在の **Chapter** にも適用されます。

## <a name="applies-to"></a>適用対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

