---
title: Bookmark プロパティ (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704771"
---
# <a name="bookmark-property-ado"></a>Bookmark プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトでカレント レコードを一意に識別するブックマークを示します。または、 **Recordset** オブジェクトのカレント レコードを、有効なブックマークで識別されるレコードに設定します。

## <a name="settings-and-return-values"></a>設定値および戻り値

有効なブックマークとして評価されるバリアント型 ( **Variant** ) の式を設定または取得します。

## <a name="remarks"></a>解説

**Bookmark** プロパティを使用すると、カレント レコードの位置を保存しておき、いつでもそのレコードに戻ることができます。ブックマークは、ブックマーク機能をサポートしている **Recordset** オブジェクトでのみ使用できます。

**Recordset** オブジェクトを開くと、各レコードには一意のブックマークが割り当てられます。カレント レコードのブックマークを保存するには、 **Bookmark** プロパティの値を変数に代入します。別のレコードに移動した後、 **Recordset** オブジェクトの **Bookmark** プロパティをその変数の値に設定すると、いつでもそのレコードに戻ることができます。

ユーザーがブックマークの値を見ることはできません。また、ブックマークを直接比較できるとは想定しないでください。同じレコードを参照する 2 つのブックマークであっても、互いに異なる値を持つ場合もあります。

[Clone](clone-method-ado.md) メソッドを使用して **Recordset** オブジェクトのコピーを作成した場合、複製元および複製された **Recordset** の **Bookmark** プロパティの設定は同一になり、相互に使用することができます。一方、異なる **Recordset** オブジェクトのブックマークは、たとえ同一のソースまたは同一のコマンドから作成したものであっても、相互に使用することはできません。

**リモート データ サービスの使用法**クライアント側の**Recordset**オブジェクトで使用すると、**ブックマーク**プロパティは常にされます。

