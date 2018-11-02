---
title: 再同期の動的なプロパティ (ADO) を更新します。
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f1443d1f2a4eccd8599256425a971bc63cd4d8b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918983"
---
# <a name="update-resync-dynamic-property-ado"></a>再同期の動的なプロパティ (ADO) を更新します。


**適用されます**Access 2013、Office 2013。

[UpdateBatch](updatebatch-method-ado.md) メソッドの後に暗黙の [Resync](resync-method-ado.md) メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。

## <a name="settings-and-return-values"></a>設定値および戻り値

いずれかを取得または設定します[ADCPROP\_UPDATERESYNC\_列挙型](adcprop-updateresync-enum.md)の値です。

## <a name="remarks"></a>備考

ADCPROP の値\_UPDATERESYNC\_既に残りの値の組み合わせを表す adResyncAll を除いて、列挙型を組み合わせることができます。

定数 **adResyncConflicts** は、再同期値を基になる値として保存しますが、保留中の変更は上書きしません。

**Update Resync** は、 [CursorLocation](recordset-object-ado.md) プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。

