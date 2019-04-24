---
title: 行プロパティ-ActiveX データオブジェクト (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306483"
---
# <a name="row-property-ado"></a>Row プロパティ (ADO)

**適用先:** Access 2013、Office 2013

**ADORecordConstruction** オブジェクトの OLE DB **Row** オブジェクトを設定または取得します。 **put\_row**を使用して**row**オブジェクトを設定すると、行は ADO **Record**オブジェクトになります。 値の取得と設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_行 (\[out, retval\] IUnknown\* \* pprow);

HRESULT put\_行 (\[\] IUnknown\* prow);

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*pprow* |OLE DB **Row** オブジェクトを指すポインター。|
|*PRow* |OLE DB **Row** オブジェクト。|

## <a name="return-values"></a>戻り値

このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。

## <a name="applies-to"></a>適用対象

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

