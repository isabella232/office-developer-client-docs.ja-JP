---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: edac057e9f8cc76d189d95019eebb969bc9c9e79
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623958"
---
# <a name="upfld"></a>UPFLD

**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロード フォルダーの状態中にフォルダーを [アップロードする場合の情報](upload-folder-state.md)です。
  
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
  
>  [out]/[in] uplaod に対する適切なアクションを決定するフラグ。 
    
  - UPF_NEW
    
    - [out]フォルダーが新しい。
    
  - UPF_MOD_PARENT
    
    - [out]フォルダーが移動されました。
    
  - UPF_MOD_PROPS
    
    - [out]フォルダーのプロパティが変更されました。
    
  - UPF_DEL
    
    - [out]フォルダーが削除されました。
    
  - UPF_OK
    
    - [in]アップロード成功しました。 クライアントは、フォルダー情報をサーバーにアップロードした後にこれを設定します。
    
_pfld_
  
> [out]アップロードする開いているフォルダー オブジェクト。
    
_feid_
  
> [out] フォルダーのエントリ ID です。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)

