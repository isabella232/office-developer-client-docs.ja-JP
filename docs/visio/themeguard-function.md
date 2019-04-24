---
title: THEMEGUARD 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: 図形の書式設定セルを保護して、現在のテーマの適切な側面を使用していることを確認します。
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326755"
---
# <a name="themeguard-function"></a>THEMEGUARD 関数

図形の書式設定セルを保護して、現在のテーマの適切な側面を使用していることを確認します。
  
## <a name="syntax"></a>構文

THEMEGUARD ()
  
## <a name="remarks"></a>解説

THEMEGUARD 関数をセルに適用しても、GUARD 関数の場合と同様、手動でフォーマットを適用することは可能です。 ユーザーインターフェイスの図形に書式を適用した場合、またはオートメーションを使用して、手動で書式設定する値を格納するために SETATREFEXPR 関数を数式に含める場合を除き、THEMEGUARD 数式は上書きされます。 
  
## <a name="example"></a>例

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

主テーマに設定された塗りつぶし色の代わりに、現在のテーマの Accent 2 の色で図形を塗りつぶすよう指定します。
  

