---
title: '[LockFromGroupFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805768"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>[LockFromGroupFormat] セル ([Protection] セクション)

フォーマットを変更してグループ図形を直接選択したサブ図形の書式を設定するユーザーを許可する一方、サブ図形に反映されません。 
  
LockFromGroupFormat セルの値は、**グループの書式設定**チェック ボックスの設定、[**保護**] ダイアログ ボックスでに対応します。 
  
別の数式または**CellsU**プロパティを使用して、プログラムから、名前で、[LockFromGroupFormat] セルへ参照するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockFromGroupFormat  <br/> |
   
LockFromGroupFormat] セルへインデックスを使用してプログラムから、参照するには、次の引数で**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockFromGroupFormat** <br/> |
   
セルの既定値は 0 (False) となります。
  

