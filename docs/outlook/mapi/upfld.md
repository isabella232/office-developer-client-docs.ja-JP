---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f25b3fb967f4ed93ac38487f21145f35413764da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804176"
---
# <a name="upfld"></a>UPFLD

**適用されます**: Outlook 
  
[フォルダーの状態をアップロード](upload-folder-state.md)する際にフォルダーをアップロードする方法の詳細については。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>メンバー

_ulFlags_
  
>  [out]/[in]、uplaod の適切なアクションを決定するフラグ。 
    
  - UPF_NEW
    
    - [out]フォルダーは、新しいです。
    
  - UPF_MOD_PARENT
    
    - [out]フォルダーに移動されました。
    
  - UPF_MOD_PROPS
    
    - [out]フォルダーのプロパティが変更されました。
    
  - UPF_DEL
    
    - [out]フォルダーが削除されました。
    
  - UPF_OK
    
    - [in]アップロードが正常に完了しました。 クライアントでは、フォルダー情報をサーバーにアップロードした後、これを設定します。
    
_pfld_
  
> [out]アップロードするフォルダーを開くオブジェクトです。
    
_feid_
  
> [out]フォルダーのエントリ ID です。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション状態マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)

