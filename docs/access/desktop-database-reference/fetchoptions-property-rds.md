---
title: FetchOptions プロパティ (RDS)
TOCTitle: FetchOptions property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa5bdd448cc46e2b665c85d8aff9b79d1c5e81e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558339"
---
# <a name="fetchoptions-property-rds"></a>FetchOptions プロパティ (RDS)


**適用先:** Access 2013、Office 2013

非同期フェッチの種類を示します。

## <a name="setting-and-return-values"></a>設定値と戻り値

次のいずれかの値を設定または取得します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcFetchUpFront</strong></p></td>
<td><p>Recordset のすべてのレコードは、 <a href="recordset-object-ado.md">コントロール</a> がアプリケーションに返される前にフェッチされます。 完全な <strong>Recordset</strong> は、アプリケーションで何かを実行する前にフェッチされます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>レコードの最初のバッチがフェッチされると、制御をアプリケーションに戻すことができます。最初のバッチでフェッチされなかったレコードへのアクセスを試みるそれ以降の <strong>Recordset</strong> の読み取りは、要求されたレコードが実際にフェッチされて制御がアプリケーションに戻るまで遅延されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>既定値です。レコードがバックグラウンドでフェッチされる間に、制御は直ちにアプリケーションに戻ります。フェッチされていないレコードをアプリケーションが読み取ろうとした場合、要求されているレコードに最も近いレコードが読み取られ、制御はすぐに戻り、現在の <strong>Recordset</strong> の最終位置に到達したことを示します。たとえば、<a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> を呼び出した場合、現在のレコードの位置は、<strong>Recordset</strong> にさらに多くのレコードが格納される予定であっても、実際にフェッチされた最後のレコードに移動します。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] これらの定数を使用するクライアント側の各実行可能ファイルで、使用する定数を宣言する必要があります。定数の宣言は、C:\Program Files\Common Files\System\MSADC フォルダーにある Adcvbs.inc ファイルからコピーして貼り付けることができます。



## <a name="remarks"></a>注釈

Web アプリケーションでは、パフォーマンスが向上するために **、通常は adcFetchAsync** (既定値) を使用する必要があります。 コンパイルされたクライアント アプリケーションでは、一般に **adcFetchBackground** を使います。

