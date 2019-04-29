---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414922"
---
# <a name="uphier"></a>UPHIER
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
[階層のアップロード状態](upload-hierarchy-state.md)でのフォルダー階層の同期に関する情報。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
> 順番フォルダー階層を同期するときの動作を変更するフラグです。
    
  - UPH_OK
    
    - 順番アップロードに成功しました。 クライアントは、サーバーに情報を正常にアップロードした後にこれを設定します。 このフラグが表示されると、Outlook は、更新が必要なフォルダー階層を示す内部のブックキーピング情報をクリアします。 
    
    - アップロードが成功しなかった場合、クライアントは HRESULT を渡します。
    
_pstmReserved_
  
> 読み上げこのメンバーは Outlook の内部使用のために予約されており、サポートされていません。
    
_ient_
  
> 読み上げで指定されたフォルダーの数を同期** するためのインデックスです。 
    
_fea-cent-logging-service_
  
> 読み上げ同期されていないフォルダーの数。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)

