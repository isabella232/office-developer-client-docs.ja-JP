---
title: fetchoptions プロパティ (RDS)
TOCTitle: FetchOptions property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd2ecf0d7d3df6d1caffd906cf318916a2a8882
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293197"
---
# <a name="fetchoptions-property-rds"></a>fetchoptions プロパティ (RDS)


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
<td><p><strong>adcfetchupfront</strong></p></td>
<td><p><a href="recordset-object-ado.md">Recordset</a>のすべてのレコードは、コントロールがアプリケーションに返される前に取得されます。 完全な<strong>Recordset</strong>は、アプリケーションですべての操作を実行できるようになる前に取得されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adcfetchbackground</strong></p></td>
<td><p>レコードの最初のバッチがフェッチされると、制御をアプリケーションに戻すことができます。最初のバッチでフェッチされなかったレコードへのアクセスを試みるそれ以降の <strong>Recordset</strong> の読み取りは、要求されたレコードが実際にフェッチされて制御がアプリケーションに戻るまで遅延されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcfetchasync</strong></p></td>
<td><p>既定値です。レコードがバックグラウンドでフェッチされる間に、制御は直ちにアプリケーションに戻ります。フェッチされていないレコードをアプリケーションが読み取ろうとした場合、要求されているレコードに最も近いレコードが読み取られ、制御はすぐに戻り、現在の <strong>Recordset</strong> の最終位置に到達したことを示します。たとえば、<a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> を呼び出した場合、現在のレコードの位置は、<strong>Recordset</strong> にさらに多くのレコードが格納される予定であっても、実際にフェッチされた最後のレコードに移動します。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] これらの定数を使用するクライアント側の各実行可能ファイルで、使用する定数を宣言する必要があります。定数の宣言は、C:\Program Files\Common Files\System\MSADC フォルダーにある Adcvbs.inc ファイルからコピーして貼り付けることができます。



## <a name="remarks"></a>注釈

web アプリケーションでは、より優れたパフォーマンスが提供されるため、通常は**adcfetchasync** (既定値) を使用します。 コンパイルされたクライアント アプリケーションでは、一般に **adcFetchBackground** を使います。

