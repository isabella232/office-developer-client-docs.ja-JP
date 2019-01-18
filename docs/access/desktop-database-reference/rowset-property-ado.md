---
title: Rowset プロパティ (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706143"
---
# <a name="rowset-property-ado"></a>Rowset プロパティ (ADO)

**適用されます**Access 2013、Office 2013。

**ADORecordsetConstruction** オブジェクトの OLE DB **Rowset** オブジェクトを取得または設定します。 Put を使用すると、\_、ADO**レコード セット**オブジェクトに、行セットの行セットが有効になっています。

値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_行セット (\[、戻り値を\]IUnknown\* \* ppRowset)。

HRESULT に\_の行セット (\[の\]IUnknown\*ため)。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ppRowset* |OLE DB **Rowset** オブジェクトを指すポインター。|
|*PRowset* |OLE DB **Rowset** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。

## <a name="applies-to"></a>適用対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

