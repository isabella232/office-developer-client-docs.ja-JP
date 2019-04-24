---
title: Flush メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292343"
---
# <a name="flush-method-ado"></a>Flush メソッド (ADO)


**適用先:** Access 2013、Office 2013

ADO バッファーに残っている [Stream](stream-object-ado.md) の内容を、**Stream** に関連付けられた、基になるオブジェクトに反映します。

## <a name="syntax"></a>構文

*ストリーム*。揃え

## <a name="remarks"></a>注釈

このメソッドを使用すると、基になるオブジェクト (たとえば、 **Stream** オブジェクトのソースの URL で表されるノードやファイル) に、ストリーム バッファーの内容を送ることができます。 **Stream** の内容に加えたすべての変更が確実に書き込まれるようにするには、このメソッドを呼び出す必要があります。ただし、ADO ではバックグラウンドで可能な限り継続してバッファーのフラッシュが行われるので、通常は **Flush** を呼び出す必要はありません。 **Stream** の内容の更新は自動的に行われ、 **Flush** を呼び出すまでキャッシュされるわけではありません。

**Close** メソッドで [Stream](close-method-ado.md) を閉じると、 **Stream** の内容が自動的にフラッシュされるので、 **Close** の直前に明示的に **Flush** を呼び出す必要はありません。

