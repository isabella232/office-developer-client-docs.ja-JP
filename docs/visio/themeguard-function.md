---
title: THEMEGUARD 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: 現在のテーマの適切な設定を使用するようにするのには図形のセルの書式設定を保護します。
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806642"
---
# <a name="themeguard-function"></a>THEMEGUARD 関数

現在のテーマの適切な設定を使用するようにするのには図形のセルの書式設定を保護します。
  
## <a name="syntax"></a>構文

THEMEGUARD()
  
## <a name="remarks"></a>注釈

THEMEGUARD 関数をセルに適用すること防ぐことはできませんが、ガードを適用する関数と同じ方法で手動で書式設定をします。 ユーザー インターフェイスまたはオートメーションを使用してプログラムを使用して、図形を書式設定する場合、THEMEGUARD 式をオーバーライドすると、手動の書式設定の値を格納する数式に、SETATREFEXPR 関数を追加する場合を除き、します。 
  
## <a name="example"></a>例

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

主テーマに設定された塗りつぶし色の代わりに、現在のテーマの Accent 2 の色で図形を塗りつぶすよう指定します。
  

