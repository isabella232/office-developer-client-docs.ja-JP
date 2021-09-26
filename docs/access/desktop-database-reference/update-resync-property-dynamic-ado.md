---
title: Update Resync dynamic property (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5eed22559b0645cdae4498438fd6926136fb3303
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631651"
---
# <a name="update-resync-dynamic-property-ado"></a>Update Resync dynamic property (ADO)


**適用先**: Access 2013、Office 2013

[UpdateBatch](updatebatch-method-ado.md) メソッドの後に暗黙の [Resync](resync-method-ado.md) メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。

## <a name="settings-and-return-values"></a>設定および戻り値

1 つ以上の [ADCPROP \_ UPDATERESYNC \_ ENUM 値を設定または返](adcprop-updateresync-enum.md) します。

## <a name="remarks"></a>注釈

ADCPROP UPDATERESYNC ENUM の値は、他の値の組み合わせを既に表している adResyncAll を除き、組み \_ \_ 合わせることができます。

定数 **adResyncConflicts** は、再同期値を基になる値として保存しますが、保留中の変更は上書きしません。

**Update Resync** は、 [CursorLocation](recordset-object-ado.md) プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。

