---
title: CreateObject メソッド (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295374"
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
<td><p>プロトコル</p></td>
<td><p><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>computername</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>インプロセス</p></td>
<td><p><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Object* |*ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。|
|*DataSpace* |新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*ProgID* |アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。|
|*awebsrvr* または *computername* |サーバービジネスオブジェクトのインスタンスが作成されるインターネットインフォメーションサービス (IIS) web サーバーを識別する URL を表す**文字列型 (String** ) の値を指定します。|

## <a name="remarks"></a>注釈

*HTTP プロトコル*は標準の web プロトコルです。*HTTPS*はセキュリティで保護された web プロトコルです。 HTTP を使用せずにローカルエリアネットワークを実行している場合は、 *DCOM プロトコル*を使用します。 *インプロセス*プロトコルは、ローカルのダイナミックリンクライブラリ (DLL) です。ネットワークを使用しません。

