---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430407"
---
# <a name="synccont"></a>SYNCCONT

**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカル ストア内の指定されたフォルダーの内容を、コンテンツの同期状態中にサーバーと同期する [情報](synchronize-contents-state.md)です。 これには、アップロードだけ、またはアップロードとダウンロードを含む完全な同期が含まれる。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
> [in]同期中に適切な動作を判断するフラグ。
    
  - UPC_OK
    
  - [in]アップロードまたは完全同期が成功しました。 クライアントは、情報をサーバーと同期した後にこれを設定します。
    
_iEnt_
  
> [out]インデックスを使用して、cEnt で指定されたフォルダー数のコンテンツの同期  _を追跡します_。
    
_cEnt_
  
> [out]レプリケートするフォルダーの数。
    
_pvReserved_
  
> このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。 
    
_ptagaReserved_
  
> このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。 
    
_psosReserved_
  
> このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)

