---
title: FieldStatusEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 007daa84e15b79d6aa82e4e1e75b1c3d2b0901ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867924"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum

**適用されます**Access 2013、Office 2013。

**Field** オブジェクトの状態を表します。

**adFieldPending\*** 値は、状態を設定する原因となった操作を示し、他の状態値と組み合わせて使用される場合があります。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldAlreadyExists</strong></p></td>
<td><p>26</p></td>
<td><p>指定したフィールドが既に存在することを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>ADO から OLE DB プロバイダーに無効な状態値が送信されたことを示します。原因としては、OLE DB 1.0 プロバイダーまたは 1.1 プロバイダー、あるいは不適切な組み合わせの <a href="value-property-ado.md">Value</a> と <a href="status-property-ado-field.md">Status</a> が考えられます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p><a href="source-property-ado-record.md">Source</a> で指定された URL のサーバーが操作を完了できなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>移動操作で、ツリーまたはサブツリーを新しい位置に移動したがソースを削除できなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>フィールドの取得または保存を行うときにデータが失われてしまうことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCantCreate</strong></p></td>
<td><p>7</p></td>
<td><p>プロバイダーの限度 (許容フィールド数など) を超えたためにフィールドを追加できなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>プロバイダーから返されたデータがフィールドのデータ型をオーバーフローしたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>データの設定時にフィールドの既定値が使われたことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16</p></td>
<td><p>指定したフィールドが存在しないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>ソースでのデータ値の設定時にこのフィールドがスキップされたことを示します。プロバイダーで値が設定されませんでした。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>計算エンティティまたは派生エンティティであるため、フィールドを編集できないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17</p></td>
<td><p>データ ソース URL に無効な文字があることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>プロバイダーが種類 VT_NULL のバリアント型 (VARIANT) の値を返し、フィールドが空でないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfieldok で</strong></p></td>
<td><p>0</p></td>
<td><p>既定値。フィールドの追加または削除が正常に行われたことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>移動またはコピー操作を実行するために必要な記憶域をプロバイダーが確保できないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingChange</strong></p></td>
<td><p>0x40000</p></td>
<td><p>フィールドが削除され、異なるデータ型を指定して再度追加されたか、以前に状態が adFieldOK であったフィールドの値が変更されたことを示します。<a href="update-method-ado.md">Update</a> メソッドの呼び出し後にフィールドの最終形式によって <a href="fields-collection-ado.md">Fields</a> コレクションが変更されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0x20000</p></td>
<td><p><strong>Delete</strong> 操作で状態が設定されたことを示します。フィールドは、<strong>Update</strong> メソッドの呼び出し後に <strong>Fields</strong> コレクションから削除するようマークされています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0x10000</p></td>
<td><p><strong>Append</strong> 操作で状態が設定されたことを示します。<strong>Field</strong> は、<strong>Update</strong> メソッドの呼び出し後に <strong>Fields</strong> コレクションに追加するようマークされています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>これに対して、0x80000</p></td>
<td><p>フィールドの状態を設定する原因となった操作をプロバイダーが判別できないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0x100000</p></td>
<td><p>フィールドの状態を設定する原因となった操作をプロバイダーが判別できず、<strong>Update</strong> メソッドの呼び出し後に <strong>Fields</strong> コレクションからフィールドが削除されることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>読み取り専用として定義されているため、フィールドを編集できないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>データ ソース内のフィールドが読み取り専用として定義されていることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>宛先 URL にオブジェクトが既に存在し、上書きできないため、プロバイダーが操作を実行できなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18</p></td>
<td><p>データ ソースが 1 つ以上の他のアプリケーションまたはプロセスによってロックされているため、プロバイダーが操作を実行できなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>ソースまたは宛先の URL が現在のレコードの範囲外であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>値がフィールドのデータ ソース スキーマ制約に違反することを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>プロバイダーが返すデータ値が符号付きで、ADO フィールド値のデータ型が符号なしであることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>データ ソースからの読み取り時に可変長データが切り捨てられたことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>データ ソースからの読み取り時にプロバイダーが値を判別できなかったことを示します。たとえば、行が作成された直後であること、列の既定値が使用不可であること、または新しい値がまだ指定されていないことが原因として考えられます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p>21</p></td>
<td><p>URL が示す記憶域ボリュームをプロバイダーが特定できないことを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

