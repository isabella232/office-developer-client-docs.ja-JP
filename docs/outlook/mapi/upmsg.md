---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa8b84e7baed74bda25ec1b20bd79fb121a838fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587573"
---
# <a name="upmsg"></a>UPMSG

**適用されます**: Outlook 2013 |Outlook 2016 
  
[メッセージの状態をアップロード](upload-message-state.md)する際に Outlook アイテムをアップロードする方法の詳細については。
  
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

## <a name="members"></a>Members

 _ulFlags_
  
> [out]/[in] アップロード中に、適切な動作を決定するフラグ。 
    
  - UPM_ASSOC
    
    - [out]項目に関連付けられています。
    
  - UPM_NEW
    
    - [out]新しい項目。 
    
  - UPM_MOV
    
    - [out]項目をここに移動しました。
    
  - UPM_MOD_PROPS
    
    - [out]アイテムのプロパティが変更されました。
    
  - UPM_HEADER
    
    - [out]メッセージ ヘッダーの項目です。
    
  - UPM_OK
    
    - [in]アップロードが正常に完了しました。 クライアントでは、情報をサーバーにアップロードした後、これを設定します。
    
  - UPM_MOVED
    
    - [in]項目が正常に移動されました。
    
  - UPM_COMMIT
    
    - [in]今すぐアップロードの状態を反映します。
    
  - UPM_DELETE
    
    - [in]アイテムを今すぐ削除します。
    
  - UPM_SAVE
    
    - [in]アイテムに変更を保存します。
    
_pmsg_
  
> [out]アイテム オブジェクトを開きます。 **LPMESSAGE**の型定義の mapidefs.h を参照してください。 
    
_meid_
  
> [out]アイテムのエントリ ID です。
    
_binReserved1_
  
> [in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_binReserved2_
  
> [in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_feid_
  
> [out]項目が移動された場合、元のフォルダーのエントリ ID です。
    
_binChg_
  
> [out]項目が移動された場合は、同期先の項目のキーを変更します。 **SBinary**の型の定義の mapidefs.h を参照してください。 
    
_binPcl_
  
> [out]項目が移動された場合は、同期先の項目の一覧を変更します。 **SBinary**の型の定義の mapidefs.h を参照してください。 
    
_skeySrc_
  
> [out]項目が移動された場合、元の項目のソースのキーです。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

