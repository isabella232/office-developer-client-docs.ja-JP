---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804214"
---
# <a name="uptbl"></a>UPTBL

**適用されます**: Outlook 
  
[テーブルの状態をアップロード](upload-table-state.md)する時にフォルダーの内容をアップロードする方法の詳細については。
  
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
  
> [in]アップロード中に適切な動作を決定するフラグを設定します。
    
  - UPT_OK
    
    - [in]アップロードが正常に完了しました。 クライアントでは、フォルダーの内容をサーバーにアップロードした後、これを設定します。
    
_pstmReserved_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pszName_
  
> [out]フォルダーの名前です。
    
_feid_
  
> [out]フォルダーのエントリ ID です。
    
_uintReserved_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_rgte_
  
> [out]フォルダーに通常 (または非表示) の項目と関連付けられている (非表示) の項目について次の情報を保持する構造体: _rgte [0]_ は通常と関連付けられているアイテムについては、 _rgte [1]_ 。 
    
   - 新しいまたは変更されたアイテムの数
   - 読み取りの項目の数 
   - 削除済みアイテムの数
    
 _iEnt_
  
> [out]_セント_で指定された変更の数をアップロードするかを追跡するためにインデックスを作成します。
    
_セント_
  
> [out]フォルダーへの変更の数です。
    
_pupmovHead_
  
> [out][UPMOV](upmov.md)構造体のチェーンです。 
    
_保持_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)
- [UPTBLE](uptble.md)

