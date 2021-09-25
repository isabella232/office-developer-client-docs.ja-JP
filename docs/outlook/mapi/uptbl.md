---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: db56cf54bf524e3d0996b35c99eee385117b0cf8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609230"
---
# <a name="uptbl"></a>UPTBL

**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロード テーブルの状態の間にフォルダーの内容を [アップロードする場合の情報](upload-table-state.md)です。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
> [in]アップロード中の適切な動作を決定するフラグ。
    
  - UPT_OK
    
    - [in]アップロード成功しました。 クライアントは、フォルダーの内容をサーバーにアップロードした後にこれを設定します。
    
_pstmReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pszName_
  
> [out] フォルダーの名前です。
    
_feid_
  
> [out] フォルダーのエントリ ID です。
    
_uintReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_rgte_
  
> [out]フォルダー内の通常の (または非表示ではない) アイテムと関連付けられた (または非表示の) アイテムに関する次の情報を保持する構造:  _rgte[0]_ は通常のアイテム用で  _、rgte[1]_ は関連付けられたアイテム用です。 
    
   - 新規または変更されたアイテムの数
   - 読み取りアイテムの数 
   - 削除済みアイテムの数
    
 _iEnt_
  
> [out]cEnt で指定された変更の数のアップロードを追跡する  _インデックス_ です。
    
_cEnt_
  
> [out]フォルダーに対する変更の数。
    
_pupmovHead_
  
> [out] [UPMOV 構造の](upmov.md) チェーン。 
    
_pReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [UPTBLE](uptble.md)

