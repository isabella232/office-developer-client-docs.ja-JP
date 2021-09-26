---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d615084e2fc379925f53d08a2dd8ddbe538111ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619513"
---
# <a name="upmsg"></a>UPMSG

**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロード メッセージの状態中にOutlookアイテムを[アップロードする場合の情報](upload-message-state.md)です。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a>メンバー

 _ulFlags_
  
> [out]/[in] アップロード中の適切な動作を判断するフラグ。 
    
  - UPM_ASSOC
    
    - [out]アイテムが関連付けられている。
    
  - UPM_NEW
    
    - [out]新しいアイテム。 
    
  - UPM_MOV
    
    - [out]アイテムがここに移動されました。
    
  - UPM_MOD_PROPS
    
    - [out]アイテムのプロパティが変更されました。
    
  - UPM_HEADER
    
    - [out]アイテムはメッセージ ヘッダーです。
    
  - UPM_OK
    
    - [in]アップロード成功しました。 クライアントは、サーバーに情報をアップロードした後にこれを設定します。
    
  - UPM_MOVED
    
    - [in]アイテムが正常に移動されました。
    
  - UPM_COMMIT
    
    - [in]今すぐアップロード状態をコミットします。
    
  - UPM_DELETE
    
    - [in]アイテムを今すぐ削除します。
    
  - UPM_SAVE
    
    - [in]アイテムに対する変更を保存します。
    
_pmsg_
  
> [out]アイテム オブジェクトを開きます。 LPMESSAGE の型定義については、mapidefs.h **を参照してください**。 
    
_meid_
  
> [out]アイテムのエントリ ID。
    
_binReserved1_
  
> [in]このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。 
    
_binReserved2_
  
> [in]このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。 
    
_feid_
  
> [out]アイテムが移動された場合、ソース フォルダーのエントリ ID。
    
_binChg_
  
> [out]アイテムが移動された場合は、移動先アイテムのキーを変更します。 SBinary の型定義については、mapidefs.h **を参照してください**。 
    
_binPcl_
  
> [out]アイテムが移動された場合は、移動先アイテムのリストを変更します。 SBinary の型定義については、mapidefs.h **を参照してください**。 
    
_skeySrc_
  
> [out]アイテムが移動された場合、ソース アイテムのソース キー。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

