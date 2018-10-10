---
title: Update Resync プロパティ -- 動的 (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16600f22084718a6b32656ebfc56d6a9be06c676
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477771"
---
# <a name="update-resync-property--dynamic-ado"></a>Update Resync プロパティ -- 動的 (ADO)


**適用されます**Access 2013 |。Office 2013

[UpdateBatch](updatebatch-method-ado.md) メソッドの後に暗黙の [Resync](resync-method-ado.md) メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。

## <a name="settings-and-return-values"></a>設定値と戻り値

いずれかを取得または設定します[ADCPROP\_UPDATERESYNC\_列挙型](adcprop-updateresync-enum.md)の値です。

## <a name="remarks"></a>備考

ADCPROP の値\_UPDATERESYNC\_既に残りの値の組み合わせを表す adResyncAll を除いて、列挙型を組み合わせることができます。

定数 **adResyncConflicts** は、再同期値を基になる値として保存しますが、保留中の変更は上書きしません。

**Update Resync** は、 [CursorLocation](recordset-object-ado.md) プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。

