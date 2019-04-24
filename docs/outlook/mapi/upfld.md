---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360481"
---
# <a name="upfld"></a>UPFLD

**適用対象**: Outlook 2013 | Outlook 2016 
  
[アップロードフォルダーの状態](upload-folder-state.md)中にフォルダーをアップロードするための情報。
  
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
  
>  [out]/[in] フラグを使用して、uて od の適切なアクションを特定します。 
    
  - UPF_NEW
    
    - 読み上げFolder は新規です。
    
  - UPF_MOD_PARENT
    
    - 読み上げフォルダーが移動されました。
    
  - UPF_MOD_PROPS
    
    - 読み上げフォルダーのプロパティが変更されました。
    
  - UPF_DEL
    
    - 読み上げフォルダーが削除されました。
    
  - UPF_OK
    
    - 順番アップロードに成功しました。 サーバーにフォルダー情報をアップロードした後、クライアントはこの設定を行います。
    
_pfld_
  
> 読み上げアップロードする開いている folder オブジェクト。
    
_feid_
  
> [out] フォルダーのエントリ ID です。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)

