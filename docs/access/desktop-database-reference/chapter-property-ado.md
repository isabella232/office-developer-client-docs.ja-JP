---
title: Chapter プロパティ (ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478782"
---
# <a name="chapter-property-ado"></a>Chapter プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013
 

OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトから取得するか、または、OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトに設定します。 使用すると**に\_章****章**オブジェクトを設定する行のサブセットになって、ADO**レコード セット**オブジェクトにします。 これにより、 **Rowset**オブジェクトのカレント チャプターが設定されます。 値の取得および設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_章 (\[、戻り値を\]長\*plChapter)。

HRESULT に\_の章 (\[に\]長 lChapter)。

## <a name="parameters"></a>パラメーター

  - *plChapter*

  - チャプターのハンドルへのポインターです。

  - *LChapter*

  - チャプターのハンドルです。

## <a name="return-values"></a>戻り値

このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。

## <a name="applies-to"></a>対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

