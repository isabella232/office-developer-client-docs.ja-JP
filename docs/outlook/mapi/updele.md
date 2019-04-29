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
  
ローカルストアで削除されたアイテムの拡張情報。 この情報は、削除の状態の[アップロード](upload-delete-status-state.md)中に使用されます。
  
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
  
> [out]/[in] アップロード中の適切な動作を決定するフラグです。
    
  - UPD_ASSOC
    
    - 読み上げ項目が関連付けられています。
    
  - UPD_MOV
    
    - 読み上げアイテムが移動されました。
    
  - UPD_OK 
    
    - 順番アップロードに成功しました。 クライアントは、情報をサーバーにアップロードした後にこれを設定します。
    
  - UPD_MOVED
    
    - 順番アイテムは正常に移動されました。
    
  - UPD_UPDATE
    
    - 順番ソースアイテムを変更済みとしてマークします。
    
  - UPD_COMMIT
    
    - 順番今すぐアップロードの状態をコミットします (エントリ 0)。
    
_skey_
  
> 読み上げアイテムのソースキー。
    
_dwreserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。
    
_binChg_
  
> 読み上げアイテムが移動された場合は、コピー先アイテムのキーを変更します。
    
_binpcl_
  
> 読み上げアイテムが移動された場合は、コピー先アイテムのリストを変更します。
    
_skeydst_
  
> 読み上げアイテムが移動された場合のコピー先アイテムのソースキー。
    
_pupmov_
  
> 読み上げアイテムが移動された場合の移動先フォルダーの情報。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

