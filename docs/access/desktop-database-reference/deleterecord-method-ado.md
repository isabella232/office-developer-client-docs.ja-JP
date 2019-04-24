---
title: DeleteRecord メソッド (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293995"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Record](record-object-ado.md) で表されるエンティティを削除します。

## <a name="syntax"></a>構文

*Record*. **DeleteRecord * * * ソース*,*非同期*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。削除するエンティティ (ファイル、ディレクトリなど) を表す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空の文字列を指定した場合、現在 [Record](record-object-ado.md) で表されているエンティティが削除されます。Record がコレクション レコード (ディレクトリなど、[RecordType](recordtype-property-ado.md) が **adCollectionRecord** であるもの) である場合は、すべての子 (サブディレクトリなど) も削除されます。|
|*Async* |省略可能です。ブール型 ( **Boolean** ) の値を指定します。 **True** のときは、削除操作が非同期で実行されることを示します。|

## <a name="remarks"></a>注釈

このメソッドの終了後、**Record** で表されているオブジェクトに対する操作が失敗する場合があります。**DeleteRecord** を呼び出した後は **Record** を閉じる必要があります。これは、プロバイダーがデータ ソースで **Record** をいつ更新するかにより、**Record** の動作が予期できなくなることがあるためです。

If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**. recordset を最新の情報に更新するには、**レコードセット**をいったん閉じてから開き直すか、または**recordset**の再[クエリ](requery-method-ado.md)を実行するか、 [Update](update-method-ado.md)メソッドと[Resync](resync-method-ado.md)メソッドを実行します。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。


