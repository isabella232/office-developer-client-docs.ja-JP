---
title: parentrow プロパティ (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287739"
---
# <a name="parentrow-property-ado"></a>parentrow プロパティ (ADO)

**適用先:** Access 2013、Office 2013

OLE DB **Row** オブジェクトのコンテナーを **ADORecordConstruction** オブジェクトに設定し、行の親が ADO **Record** オブジェクトに変換されるようにします。

値の設定のみ可能です。

## <a name="syntax"></a>構文

HRESULT put\_parentrow (\[\] IUnknown\* pparent)。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*pparent* |行のコンテナー。|

## <a name="return-values"></a>戻り値

このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。

## <a name="applies-to"></a>適用対象

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

