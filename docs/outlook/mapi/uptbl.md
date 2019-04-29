---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438114"
---
# <a name="uptbl"></a>UPTBL

**適用対象**: Outlook 2013 | Outlook 2016 
  
[テーブルのアップロード状態](upload-table-state.md)中にフォルダーのコンテンツをアップロードするための情報。
  
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
  
> 順番アップロード中の適切な動作を決定するフラグ。
    
  - UPT_OK
    
    - 順番アップロードに成功しました。 クライアントは、フォルダーの内容をサーバーにアップロードした後に、これを設定します。
    
_pstmReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pszName_
  
> [out] フォルダーの名前です。
    
_feid_
  
> [out] フォルダーのエントリ ID です。
    
_uintReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_rgte_
  
> 読み上げ_rgte [0]_ が通常のアイテムに対して、および関連付けられている (または非表示の) アイテムに対して次の情報を保持する構造。 _rgte [1]_ は関連アイテム用です。 
    
   - 新規または変更されたアイテムの数
   - 読み取りアイテム数 
   - 削除済みアイテムの数
    
 _ient_
  
> 読み上げで指定された変更数をアップロードする__ 追跡対象のインデックス。
    
_fea-cent-logging-service_
  
> 読み上げフォルダーに対する変更の数。
    
_pupmovHead_
  
> 読み上げ[upmov](upmov.md)構造体のチェーン。 
    
_保持され_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [UPTBLE](uptble.md)

