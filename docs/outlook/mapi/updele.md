---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566587"
---
# <a name="updele"></a>UPDELE

**適用されます**: Outlook 2013 |Outlook 2016 
  
ローカル ストアで削除済みアイテムの情報を拡張します。 [アップロード ステータスの状態を削除](upload-delete-status-state.md)する時にこの情報が使用されます。
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [out]/[in] アップロード中に、適切な動作を決定するフラグ。
    
  - UPD_ASSOC
    
    - [out]項目に関連付けられています。
    
  - UPD_MOV
    
    - [out]項目移動されました。
    
  - UPD_OK 
    
    - [in]アップロードが正常に完了しました。 クライアントでは、情報をサーバーにアップロードした後、これを設定します。
    
  - UPD_MOVED
    
    - [in]項目が正常に移動されました。
    
  - UPD_UPDATE
    
    - [in]変更、ソース項目をマークします。
    
  - UPD_COMMIT
    
    - [in]アップロード状態ようになりました (項目 0) をコミットします。
    
_skey_
  
> [out]ソース項目のキー。
    
_dwReserved_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
_binChg_
  
> [out]項目が移動された場合は、同期先項目のキーを変更します。
    
_binPcl_
  
> [out]項目が移動された場合は、同期先項目の一覧を変更します。
    
_skeyDst_
  
> [out]同期先項目の項目のソースのキーに移動されました。
    
_pupmov_
  
> [out]アイテムのコピー先フォルダーの情報を移動するとします。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

