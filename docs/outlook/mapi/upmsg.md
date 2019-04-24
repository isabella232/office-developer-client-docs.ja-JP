---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338872"
---
# <a name="upmsg"></a>UPMSG

**適用対象**: Outlook 2013 | Outlook 2016 
  
[アップロードメッセージの状態](upload-message-state.md)中に Outlook アイテムをアップロードするための情報。
  
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
  
> [out]/[in] フラグを指定して、アップロード中の適切な動作を決定します。 
    
  - UPM_ASSOC
    
    - 読み上げ項目が関連付けられています。
    
  - UPM_NEW
    
    - 読み上げ新しいアイテム。 
    
  - UPM_MOV
    
    - 読み上げアイテムはここに移動されました。
    
  - UPM_MOD_PROPS
    
    - 読み上げアイテムのプロパティが変更されました。
    
  - UPM_HEADER
    
    - 読み上げアイテムはメッセージヘッダーです。
    
  - UPM_OK
    
    - 順番アップロードに成功しました。 クライアントは、情報をサーバーにアップロードした後にこれを設定します。
    
  - UPM_MOVED
    
    - 順番アイテムは正常に移動されました。
    
  - UPM_COMMIT
    
    - 順番今すぐアップロードの状態をコミットします。
    
  - UPM_DELETE
    
    - 順番今すぐアイテムを削除します。
    
  - UPM_SAVE
    
    - 順番アイテムへの変更を保存します。
    
_pmsg_
  
> 読み上げアイテムオブジェクトを開きます。 **lpmessage**の種類の定義については、「mapidefs.h」を参照してください。 
    
_meid_
  
> 読み上げアイテムのエントリ ID。
    
_binReserved1_
  
> 順番このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
_binReserved2_
  
> 順番このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
_feid_
  
> 読み上げアイテムが移動された場合は、ソースフォルダーのエントリ ID。
    
_binChg_
  
> 読み上げアイテムが移動された場合は、コピー先アイテムのキーを変更します。 **sbinary**の型定義については、「mapidefs.h」を参照してください。 
    
_binpcl_
  
> 読み上げアイテムが移動された場合は、コピー先アイテムのリストを変更します。 **sbinary**の型定義については、「mapidefs.h」を参照してください。 
    
_skeysrc_
  
> 読み上げアイテムが移動された場合は、ソースアイテムのソースキー。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

