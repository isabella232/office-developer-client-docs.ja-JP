---
title: CreateObject メソッド (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e5e3fb18aad122d7e4ef5174b724c9fce5a3f729
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565654"
---
# <a name="createobject-method-rds"></a>CreateObject メソッド (RDS)

**適用先:** Access 2013、Office 2013

目的のビジネス オブジェクトのプロキシを作成し、そのポインターを返します。プロキシは、インターネット上で要求やデータを送信するビジネス オブジェクトと交信するために、データをパッケージ化し、サーバー側スタブにマーシャリングします。インプロセス コンポーネント オブジェクトでは、プロキシは使用されず、オブジェクトへのポインターのみが返されます。

## <a name="syntax"></a>構文

RDS は、HTTP、HTTPS (HTTP over Secure Socket Layer)、DCOM、およびインプロセスのプロトコルをサポートします。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロトコル</p></th>
<th><p>構文</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP</p></td>
<td><p>オブジェクト<em></em>  =  <em>DataSpace を設定します</em>。CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>オブジェクト<em></em>  =  <em>DataSpace を設定します</em>。CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>オブジェクト<em></em>  =  <em>DataSpace を設定します</em>。CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>インプロセス</p></td>
<td><p>オブジェクト<em></em>  =  <em>DataSpace を設定します</em>。CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Object* |*ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。|
|*DataSpace* |新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*ProgID* |アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。|
|*awebsrvr* または *computername* |サーバー ビジネス オブジェクトのインスタンスが作成インターネット インフォメーション サービス(IIS) Web サーバーを識別する URL を表す文字列型 **(String)** の値。|

## <a name="remarks"></a>注釈

*HTTP プロトコルは* 標準の Web プロトコルです。*HTTPS* はセキュリティで保護された Web プロトコルです。 HTTP なしでローカル エリア ネットワークを実行する場合は *、DCOM* プロトコルを使用します。 イン *プロセス プロトコルは* 、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークは使用しない。

