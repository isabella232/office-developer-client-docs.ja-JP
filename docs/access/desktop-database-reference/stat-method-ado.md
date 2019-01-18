---
title: Stat メソッドの ActiveX データ オブジェクト (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721074"
---
# <a name="stat-method-ado"></a>Stat メソッド (ADO)

**適用されます**Access 2013、Office 2013。

**Stream** オブジェクトの情報を取得します。

## <a name="syntax"></a>構文

長*ストリーム*。Stat (*StatStg*、 *StatFlag*)

## <a name="return-value"></a>戻り値

操作の状態を示す長整数型 (Long) の値。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*StatStg* |ストリームの情報が格納される STATSTG 構造体。ADO の Stream オブジェクトに使用される Stat メソッドの実装は、この構造体のすべてのフィールドに情報を格納するわけではありません。|
|*StatFlag* |STATSTG 構造体の一部のメンバーが返されないように指定して、メモリ割り当て操作を少なくします。このパラメーターには、STATFLAG 列挙の値を指定します。<br/><br/>STATFLAG 列挙型には、2 つの値があります。<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>解説

ADO の Stream オブジェクト用に実装された Stat メソッドは、STATSTG 構造体の以下のフィールドに値を格納します。

|フィールド|説明|
|:--------|:----------|
|*pwcsName* |STATFLAG の値がある場合、ストリームの名前を含む文字列と、StatFlag\_NONAME は指定されませんでした。|
|*cbSize* |ストリームまたはバイト配列のバイト単位でのサイズを示します。|
|*mtime* |この記憶域、ストリーム、またはバイト配列の最終変更時刻を示します。|
|*ctime* |この記憶域、ストリーム、またはバイト配列の作成時刻を示します。|
|*atime* |この記憶域、ストリーム、またはバイト配列の最終アクセス時刻を示します。|

場合 STATFLAG\_NONAME StatFlag パラメーターで指定すると、ストリームの名前は返されません。

場合 STATFLAG\_NONAME は、StatFlag パラメーターで指定されていませんし、ストリームの現在の名前がないは、E\_NOTIMPL。

