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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702846"
---
# <a name="createobject-method-rds"></a>CreateObject メソッド (RDS)

**適用されます**Access 2013、Office 2013。

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
<td><p><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>https://awebsrvr</em> &quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>https://awebsrvr</em> &quot;)</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot;<em>コンピューター名</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>インプロセス</p></td>
<td><p><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Object* |*ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。|
|*DataSpace* |新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*ProgID* |アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。|
|*awebsrvr*または*コンピューター名* |サーバー ビジネス オブジェクトのインスタンスを作成する、インターネット インフォメーション サービス (IIS) web サーバーを識別する URL を表す**文字列**値。|

## <a name="remarks"></a>注釈

*HTTP プロトコル*は、標準の web プロトコルです。*HTTPS*は、セキュリティで保護された web プロトコルです。 HTTP なしのローカル ・ エリア ・ ネットワークを実行している場合は、 *DCOM プロトコル*を使用します。 *プロセス内*のプロトコルは、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークを使用しません。

