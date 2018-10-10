---
title: ParentRow プロパティ (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479687"
---
# <a name="parentrow-property-ado"></a>ParentRow プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013


OLE DB **Row** オブジェクトのコンテナーを **ADORecordConstruction** オブジェクトに設定し、行の親が ADO **Record** オブジェクトに変換されるようにします。

値の設定のみ可能です。

## <a name="syntax"></a>構文

HRESULT に\_ParentRow (\[の\]IUnknown\* pParent)。

## <a name="parameters"></a>パラメーター

  - *pParent*

  - 行のコンテナー。

## <a name="return-values"></a>戻り値

このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。

## <a name="applies-to"></a>対象

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

