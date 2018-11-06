---
title: Recordset2.Update メソッド (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 996686501d355555814a48bc665f3eb634a74298
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998617"
---
# <a name="recordset2update-method-dao"></a>Recordset2.Update メソッド (DAO)

**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。更新 (***UpdateType***、***力***)

*式***Recordset2**オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>[設定] で指定されている更新の種類を示す <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> クラスの定数です (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>ブール型 (Boolean)</strong></p></td>
<td><p><a href="recordset-addnew-method-dao.md"><strong>AddNew</strong></a> 、 <a href="fields-delete-method-dao.md"><strong>Delete</strong></a> 、または <a href="recordset2-edit-method-dao.md"><strong>Edit</strong></a> の呼び出し後に、基になるデータが他のユーザーによって変更されたかどうかにかかわらず、変更を強制的にデータベースに反映するかどうかを示すブール型 ( <strong>Boolean</strong> ) の値です。 <strong>True</strong> に設定すると、変更が強制的に反映され、他のユーザーによる変更は単純に上書きされます。 <strong>False</strong> (既定値) に設定すると、更新が保留されている間に他のユーザーが変更を加えた場合、競合する変更の更新が失敗します。エラーは発生しませんが、 <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> プロパティと <strong>BatchCollisions</strong> プロパティに、競合の数と競合によって影響を受ける行が、それぞれ格納されます (ODBCDirect ワークスペースのみ)。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Update** は、カレント レコードと、それに加えた変更を保存するために使用します。

> [!IMPORTANT]
> [!重要] 次の場合は、カレント レコードに対する変更が失われます。
> - **Edit** メソッドまたは **AddNew** メソッドを使用した後、先に **Update** を使用せずに他のレコードに移動した場合。
> - **Edit** または **AddNew** を使用した後、先に **Update** を使用せずに、再度 **Edit** または **AddNew** を使用した場合。
> - **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを他のレコードに設定した場合。
> - 先に **Update** を使用せずに **Recordset** を閉じた場合。
> - [**CancelUpdate**](recordset2-cancelupdate-method-dao.md) を使用して **Edit** 操作を取り消した場合。

レコードを編集するには、 **Edit** メソッドを使用して、カレント レコードの内容をコピー バッファーにコピーします。先に **Edit** を使用せずに、 **Update** を使用した場合や、フィールドの値を変更しようとした場合は、エラーが発生します。

ODBCDirect ワークスペースでは、カーソル ライブラリが一括更新をサポートしており、 **Recordset** を開くときにオプションとして一括更新時の共有的ロックが指定されている場合に、一括更新を実行できます。

Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **LockEdits** プロパティが **True** に設定されている場合 (排他的ロック)、 **Edit** が使用された時点から、 **Update** メソッドが実行されるか、編集が取り消されるまで、レコードがロックされます。 **LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースに反映される直前に、編集前のレコードと比較されます。 **Edit** メソッドを使用した時点からレコードが変更されている場合は、 **Update** 操作が失敗します。 Microsoft Office Access データベース エンジンに接続されている ODBC データベース、およびインストール可能な ISAM データベースでは、常に共有的ロックが使用されます。 変更による **Update** 操作を引き続き実行するには、 **Update** メソッドを再度使用します。 変更を他のユーザーのレコードを元に戻す、Move 0 を使用して現在のレコードを更新します。

> [!NOTE]
> [!メモ] レコードを追加、編集、または削除するには、基になるデータ ソースでレコードに一意なインデックスが付けられている必要があります。このようなインデックスがない場合、Microsoft Access ワークスペースで **AddNew**、 **Delete**、または **Edit** の各メソッドを呼び出すと、"アクセスが拒否されました。" というエラーが発生し、ODBCDirect ワークスペースで **Update** を呼び出すと、"引数が無効です。" というエラーが発生します。


