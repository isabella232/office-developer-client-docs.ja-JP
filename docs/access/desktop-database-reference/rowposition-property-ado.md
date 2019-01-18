---
title: RowPosition プロパティ (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720962"
---
# <a name="rowposition-property-ado"></a>RowPosition プロパティ (ADO)

**適用されます**Access 2013、Office 2013。

**ADORecordsetConstruction** オブジェクトの OLE DB **RowPosition** オブジェクトを取得または設定します。 使用すると**に\_RowPosition** **RowPosition**オブジェクトを設定するには、結果の**Recordset**オブジェクトでは、現在の行を特定するのには**RowPosition**オブジェクトを使用します。

値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_RowPosition (\[、戻り値を\]IUnknown\* \* ppRowPos)。

HRESULT に\_RowPosition (\[の\]IUnknown\* pRowPos)。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ppRowPos* |OLE DB **RowPosition** オブジェクトを指すポインター。|
|*PRowPos* |OLE DB **RowPosition** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。

## <a name="remarks"></a>解説

このプロパティを設定したときに、 **RowPosition** オブジェクトの **Rowset** オブジェクトと **Recordset** オブジェクトの **Rowset** オブジェクトが異なる場合、前者が後者よりも優先されます。同様の動作が **RowPosition** の現在の **Chapter** にも適用されます。

## <a name="applies-to"></a>適用対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

