---
title: DeleteRecord メソッド (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9dd9c5b6681732ec50442f7a4bcd9874ecf4e493
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878997"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord メソッド (ADO)


**適用されます**Access 2013、Office 2013。



[Record](record-object-ado.md) で表されるエンティティを削除します。

## <a name="syntax"></a>構文

*レコード***関係する。 ソース*、*非同期*。

## <a name="parameters"></a>パラメーター

  - *Source*

  - 省略可能です。削除するエンティティ (ファイル、ディレクトリなど) を表す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空の文字列を指定した場合、現在 [Record](record-object-ado.md) で表されているエンティティが削除されます。Record がコレクション レコード (ディレクトリなど、[RecordType](recordtype-property-ado.md) が **adCollectionRecord** であるもの) である場合は、すべての子 (サブディレクトリなど) も削除されます。

  - *Async*

  - 省略可能です。ブール型 ( **Boolean** ) の値を指定します。 **True** のときは、削除操作が非同期で実行されることを示します。

## <a name="remarks"></a>解説

このメソッドの終了後、 **Record** で表されているオブジェクトに対する操作が失敗する場合があります。 **DeleteRecord** を呼び出した後は **Record** を閉じる必要があります。これは、プロバイダーがデータ ソースで **Record** をいつ更新するかにより、 **Record** の動作が予期できなくなることがあるためです。

この**レコード**を[レコード セット](recordset-object-ado.md)から取得した場合、この操作の結果は反映されませんすぐに**レコード セット**で。 閉じて、再度開いたとき、または**レコード セット**は、[クエリを再実行](requery-method-ado.md)、または[更新](update-method-ado.md)し、[再同期](resync-method-ado.md)の方法を実行することによって、**レコード セット**を更新します。


> [!NOTE]
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。


