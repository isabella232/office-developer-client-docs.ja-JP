---
title: State プロパティ (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5e6d8dbad4245e68fb18cbc5c90dab54d4466601
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593545"
---
# <a name="state-property-ado-md"></a>State プロパティ (ADO MD)


**適用先**: Access 2013、Office 2013

セルセットの現在の状態を示します。

## <a name="return-values"></a>戻り値

[Cellset](cellset-object-ado-md.md) オブジェクトの現在の状態を示す長整数型 (**Long**) の値を取得します。値の取得のみが可能です。有効な値は、**adStateClosed** (0) および **adStateOpen** (1) です。

## <a name="remarks"></a>注釈

[ObjectStateEnum](objectstateenum.md) 定数の名前を使用するには、プロジェクトで ADO タイプ ライブラリが参照されている必要があります。詳細については、「[ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)」を参照してください。

