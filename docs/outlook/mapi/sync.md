---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433809"
---
# <a name="sync"></a>SYNC

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカル ストアとサーバー間の同期を開始する情報。 この情報は、同期状態の間 [に使用されます](synchronize-state.md)。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a>メンバー

 _ulFlags_
  
- [out]/[in] 同期中の動作を変更する次のフラグのビットマスク。
    
- UPS_UPLOAD_ONLY
    
  - [in]クライアントはアップロードのみを実行します。 Outlook変更されたフォルダーのみを返します。
    
- UPS_DNLOAD_ONLY
    
  - [in]クライアントはダウンロードのみを実行します。 Outlookのアップロード ビットをクリアしない必要があります。
    
- UPS_THESE_FOLDERS
    
  - [in]クライアントは、指定された一連のフォルダーを、指定されたエントリ ID と同期します。 このフラグは、UPS_UPLOAD_ONLY **またはUPS_DNLOAD_ONLY****できます。** 
    
- UPS_OK
    
  - [out]同期が成功しました。 クライアントは、アップロード後、または完全同期が完了した後にこれを設定します。
    
- 
    
    > [!NOTE]
    > クライアントは、レプリケーション API とフォルダーとアイテムをアップロードまたは完全に同期 (アップロードしてからダウンロード) することもできますが、クライアントは **、UPS_UPLOAD_ONLY** フラグまたは UPS_DNLOAD_ONLY フラグのいずれかである一度にレプリケーションの方向が 1 つのみ *ulFlags* **を指定** します。 完全同期の場合、クライアントは最初に UPS_UPLOAD_ONLY フラグを使用してアップロードを行い、次に UPS_DNLOAD_ONLY フラグ **をUPS_DNLOAD_ONLY** します。 
  
 _pwzPath_
  
- [out]ローカル ストアへのパス。
    
 _Reserved1_
  
- このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。
    
 _Reserved2_
  
- このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。
    
 *pel* 
  
- [in]これは、フォルダーが設定されている場合に同期するフォルダー **UPS_THESE_FOLDERS** 一覧です。 **LPENTRYLIST** の型定義については、mapidefs.h を参照してください。 
    
 _pulFolderOptions_
  
- [in]これは、プロパティが設定されている場合、pel 内の **対応するフォルダー UPS_THESE_FOLDERS** 配列です。 これらのフォルダー オプションは、アップロード フォルダーの状態の間に  *pel*  にリストされている各フォルダーをアップロード [するときに使用されます](upload-folder-state.md)。 フォルダー オプションの詳細については **[、「UPFLD」を参照してください](upfld.md)**。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)

