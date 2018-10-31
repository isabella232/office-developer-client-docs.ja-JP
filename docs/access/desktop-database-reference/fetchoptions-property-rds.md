---
title: FetchOptions プロパティ (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3e7251ba50b003b37cdeb0dd70fe4a98821d4c9
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861933"
---
# <a name="fetchoptions-property-rds"></a>FetchOptions プロパティ (RDS)


**適用されます**Access 2013 |。Office 2013

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
<td><p>Recordset のすべてのレコードは、制御がアプリケーションに返される前にフェッチされます。アプリケーションで Recordset を操作できるように、事前に Recordset 全体がフェッチされます。</p></td>
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



## <a name="remarks"></a>解説

<<<<<<< ヘッド Web アプリケーションは通常使用する**adcFetchAsync** (既定値) の場合より優れたパフォーマンスを提供するためです。 コンパイルされたクライアント アプリケーションでは、一般に **adcFetchBackground** を使います。
=== Web アプリケーションでは通常使用する**adcFetchAsync** (既定値) の場合より優れたパフォーマンスを提供するためです。 コンパイルされたクライアント アプリケーションでは、一般に **adcFetchBackground** を使います。
>>>>>>> master

