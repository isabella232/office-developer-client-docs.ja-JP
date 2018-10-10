---
title: 行のプロパティを ActiveX データ オブジェクト (ADO)
TOCTitle: Row Property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05d97bb411c4199677f512d9412653ca5a4b4fe1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477638"
---
# <a name="row-property-ado"></a>Row プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013



**ADORecordConstruction** オブジェクトの OLE DB **Row** オブジェクトを設定または取得します。 使用すると**に\_行****行**オブジェクトを設定するのには、行になって ADO**レコード**オブジェクトにします。 値の取得および設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_行 (\[、戻り値を\]IUnknown\* \* ppRow)。

HRESULT に\_の行 (\[の\]IUnknown\* pRow)。

## <a name="parameters"></a>パラメーター

  - *ppRow*

  - OLE DB **Row** オブジェクトを指すポインター。

  - *PRow*

  - OLE DB **Row** オブジェクト。

## <a name="return-values"></a>戻り値

このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。

## <a name="applies-to"></a>対象

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

