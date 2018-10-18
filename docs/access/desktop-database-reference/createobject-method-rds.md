---
title: CreateObject メソッド (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602721"
---
# <a name="createobject-method-rds"></a>CreateObject メソッド (RDS)


**適用されます**Access 2013 |。Office 2013


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

  - *Object*

  - *ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。

  - *インスタンス*

  - 新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。

  - *ProgID*

  - アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。

  - *awebsrvr*または*コンピューター名*

<<<<<<< ヘッド
  - サーバー ビジネス オブジェクトのインスタンスが作成される、インターネット インフォメーション サービス (IIS) Web サーバーを識別する URL を表す文字列型 ( **String** ) の値を指定します。

## <a name="remarks"></a>解説

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a>*HTTP プロトコル*は、標準の Web プロトコルです。*HTTPS*は、セキュリティで保護された Web プロトコルです。 HTTP なしのローカル ・ エリア ・ ネットワークを実行している場合は、 *DCOM プロトコル*を使用します。 *プロセス内*のプロトコルは、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークを使用しません。
=======
  - サーバー ビジネス オブジェクトのインスタンスを作成する、インターネット インフォメーション サービス (IIS) web サーバーを識別する URL を表す**文字列**値。

## <a name="remarks"></a>備考

*HTTP プロトコル*は、標準の web プロトコルです。*HTTPS*は、セキュリティで保護された web プロトコルです。 HTTP なしのローカル ・ エリア ・ ネットワークを実行している場合は、 *DCOM プロトコル*を使用します。 *プロセス内*のプロトコルは、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークを使用しません。
>>>>>>> master

