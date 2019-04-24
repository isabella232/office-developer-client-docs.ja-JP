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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306742"
---
# <a name="rowset-property-ado"></a>Rowset プロパティ (ADO)

**適用先:** Access 2013、Office 2013

**ADORecordsetConstruction** オブジェクトの OLE DB **Rowset** オブジェクトを取得または設定します。 put\_行セットを使用すると、行セットは ADO **Recordset**オブジェクトになります。

値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_行セット\[(out,\] retval\* \* IUnknown ppRowset);

HRESULT put\_行セット\[(\] IUnknown\* pRowset)。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ppRowset* |OLE DB **Rowset** オブジェクトを指すポインター。|
|*PRowset* |OLE DB **Rowset** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。

## <a name="applies-to"></a>適用対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

