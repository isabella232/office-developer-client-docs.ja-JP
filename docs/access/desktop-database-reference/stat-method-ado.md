---
title: Stat メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308551"
---
# <a name="stat-method-ado"></a>Stat メソッド (ADO)

**適用先:** Access 2013、Office 2013

**Stream** オブジェクトの情報を取得します。

## <a name="syntax"></a>構文

長い*ストリーム*。Stat (*StatStg*, *statflag*)

## <a name="return-value"></a>戻り値

操作の状態を示す長整数型 (Long) の値。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*StatStg* |ストリームの情報が格納される STATSTG 構造体。ADO の Stream オブジェクトに使用される Stat メソッドの実装は、この構造体のすべてのフィールドに情報を格納するわけではありません。|
|*StatFlag* |STATSTG 構造体の一部のメンバーが返されないように指定して、メモリ割り当て操作を少なくします。このパラメーターには、STATFLAG 列挙の値を指定します。<br/><br/>statflag 列挙体には、次の2つの値があります。<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>注釈

ADO の Stream オブジェクト用に実装された Stat メソッドは、STATSTG 構造体の以下のフィールドに値を格納します。

|Field|説明|
|:--------|:----------|
|*pwcsName* |ストリームの名前を含む文字列。使用可能な場合、statflag の値 statflag フラグ\_が指定されていない場合。|
|*cbSize* |ストリームまたはバイト配列のバイト単位でのサイズを示します。|
|*mtime* |この記憶域、ストリーム、またはバイト配列の最終変更時刻を示します。|
|*ctime* |この記憶域、ストリーム、またはバイト配列の作成時刻を示します。|
|*atime* |この記憶域、ストリーム、またはバイト配列の最終アクセス時刻を示します。|

\_statflag が statflag パラメーターで指定されている場合、ストリームの名前は返されません。

\_statflag が statflag パラメーターで指定されておらず、現在のストリームに使用できる名前がない場合、この値は E\_NOTIMPL になります。

