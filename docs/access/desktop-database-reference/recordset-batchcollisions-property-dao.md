---
title: Recordset.BatchCollisions プロパティ (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: adcecada39d5e30c148a0531fd56d86a8e3c20de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562385"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Recordset.BatchCollisions プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .BatchCollisions

*expression*: **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

このプロパティには、最後に実行を試みられたバッチ **[Update](recordset-update-method-dao.md)** の呼び出し中に競合が発生した行へのブックマークの配列が含まれます。 **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** プロパティは、配列の要素の数を示します。

作業中の **[Recordset](recordset-object-dao.md)** オブジェクトの **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを、 **BatchCollisions** 配列のブックマークの値に設定すると、最新のバッチモードの Update 操作の完了に失敗した各レコードに移動できます。

競合するレコードを修正した後、バッチモードの **Update** メソッドを再び呼び出すことができます。ここで DAO はもう一度バッチ更新を試み、再び **BatchCollisions** プロパティに、2 回目の実行で失敗したレコードのセットが反映されます。以前の実行が正常に終了したレコードは、 **[RecordStatus](recordset-recordstatus-property-dao.md)** プロパティが dbRecordUnmodified に設定されているため、現在の実行には送信されません。このプロセスは、競合が発生する限り続行できますが、更新を中止して結果セットを閉じることもできます。

この配列は、バッチ モード **Update** メソッドを実行するたびに再作成されます。

