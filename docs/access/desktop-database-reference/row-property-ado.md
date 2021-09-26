---
title: Row プロパティ - ActiveX データ オブジェクト (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c21d714c13fb3b706f932e3cb1248f2d4e2874f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611582"
---
# <a name="row-property-ado"></a>Row プロパティ (ADO)

**適用先**: Access 2013、Office 2013

**ADORecordConstruction** オブジェクトの OLE DB **Row** オブジェクトを設定または取得します。 Put Row オブジェクト **\_ を使用して** **Row** オブジェクトを設定すると、行は ADO Record オブジェクトに **変換** されます。 値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get \_ Row( \[ out, retval \] IUnknown \* \* ppRow);

HRESULT put \_ Row( \[ in \] IUnknown \* pRow);

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ppRow* |OLE DB **Row** オブジェクトを指すポインター。|
|*PRow* |OLE DB **Row** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティ メソッドは、標準の HRESULT 値 (S \_ OK、E FAIL など) を返 \_ します。

## <a name="applies-to"></a>適用対象

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

