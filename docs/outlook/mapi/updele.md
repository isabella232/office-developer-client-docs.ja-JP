---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424883"
---
# <a name="updele"></a>UPDELE

**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカル ストアで削除されたアイテムの拡張情報。 この情報は、アップロードの削除状態 [の間に使用されます](upload-delete-status-state.md)。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
> [out]/[in] アップロード時の適切な動作を判断するフラグ。
    
  - UPD_ASSOC
    
    - [out]アイテムが関連付けられている。
    
  - UPD_MOV
    
    - [out]アイテムが移動されました。
    
  - UPD_OK 
    
    - [in]アップロード成功しました。 クライアントは、サーバーに情報をアップロードした後にこれを設定します。
    
  - UPD_MOVED
    
    - [in]アイテムが正常に移動されました。
    
  - UPD_UPDATE
    
    - [in]変更済みとしてソース アイテムをマークします。
    
  - UPD_COMMIT
    
    - [in]アップロードの状態を今すぐコミットします (エントリ 0)。
    
_skey_
  
> [out]アイテムのソース キー。
    
_dwReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。
    
_binChg_
  
> [out]アイテムが移動されている場合は、移動先アイテムのキーを変更します。
    
_binPcl_
  
> [out]アイテムが移動されている場合は、移動先アイテムのリストを変更します。
    
_skeyDst_
  
> [out]アイテムが移動されている場合の移動先アイテムのソース キー。
    
_pupmov_
  
> [out]アイテムが移動された場合の移動先フォルダー情報。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

