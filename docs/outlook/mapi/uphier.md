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
  
アップロード階層の状態中にフォルダー階層を [同期する場合の情報](upload-hierarchy-state.md)です。
  
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
  
> [in]フォルダー階層を同期するときに動作を変更するフラグ。
    
  - UPH_OK
    
    - [in]アップロード成功しました。 クライアントは、サーバーに情報を正常にアップロードした後にこれを設定します。 このフラグを表示すると、Outlook更新が必要なフォルダー階層を示す内部簿記情報が消去されます。 
    
    - アップロードが成功しなかった場合、クライアントは HRESULT を渡します。
    
_pstmReserved_
  
> [out]このメンバーは、内部Outlookのために予約され、サポートされていません。
    
_iEnt_
  
> [out]cEnt で指定されたフォルダー数の同期を追跡する  *インデックス*  です。 
    
_cEnt_
  
> [out]同期外のフォルダーの数。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)

