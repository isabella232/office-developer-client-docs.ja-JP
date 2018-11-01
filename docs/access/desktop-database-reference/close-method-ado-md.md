---
title: Close メソッド (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28c5ff23470015c9b40c996a1eb5b60f74766da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888791"
---
# <a name="close-method-ado-md"></a>Close メソッド (ADO MD)


**適用されます**Access 2013、Office 2013。

開いているセルセットを閉じます。

## <a name="syntax"></a>構文

*セルセット*。閉じる

## <a name="remarks"></a>解説

**Close** メソッドを使用して [Cellset](cellset-object-ado-md.md) オブジェクトを閉じると、関連するすべての [Cell](cell-object-ado-md.md)、[Axis](axis-object-ado-md.md)、[Position](position-object-ado-md.md)、または [Member](member-object-ado-md.md) オブジェクトのデータを含む、関連付けられたデータが解放されます。 **Cellset** を閉じてもメモリからは削除されないため、プロパティの設定を変更したり、後から再び開くことが可能です。オブジェクトをメモリから完全に削除するには、オブジェクト変数を **Nothing** に設定します。

後から [Open](open-method-ado-md.md) メソッドを呼び出して、同じまたは異なるソース文字列を使用する **Cellset** を再び開くことができます。 **Cellset** オブジェクトが閉じている間に、基になるデータまたはメタデータを参照するプロパティを取得したりメソッドを呼び出したりすると、エラーが発生します。

