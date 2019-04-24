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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349596"
---
# <a name="sync"></a>SYNC

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカルストアとサーバーの間の同期を開始するための情報。 この情報は、[同期状態](synchronize-state.md)の間に使用されます。
  
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
    
  - 順番クライアントはアップロードのみを実行します。 Outlook は、ローカルで変更されたフォルダーのみを返します。
    
- UPS_DNLOAD_ONLY
    
  - 順番クライアントはダウンロードのみを実行します。 Outlook では、フォルダーのアップロードビットをクリアすることはできません。
    
- UPS_THESE_FOLDERS
    
  - 順番クライアントは、指定されたフォルダーのセットと指定されたエントリ id を同期します。 このフラグは、 **UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**のいずれかのフラグと組み合わせて使用できます。 
    
- UPS_OK
    
  - 読み上げ同期に成功しました。 クライアントは、アップロード後または完全同期の完了後にこれを設定します。
    
- 
    
    > [!NOTE]
    > クライアントは、レプリケーション API を使用してフォルダーとアイテムをアップロードまたは完全に同期 (アップロードしてからダウンロード) することができますが、クライアントは一度にレプリケーションの方向が1つだけの*ulflags*を指定します ( **UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**フラグ。 完全同期の場合、クライアントはまず**UPS_UPLOAD_ONLY**フラグを使用してアップロードを行い、 **UPS_DNLOAD_ONLY**フラグを使用してダウンロードします。 
  
 _pwzPath_
  
- 読み上げローカルストアへのパス。
    
 _Reserved1_
  
- このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。
    
 _Reserved2_
  
- このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。
    
 *bpel* 
  
- 順番これは、 **UPS_THESE_FOLDERS**が設定されている場合に同期するフォルダーのエントリ id の一覧です。 **lmapidefs.h trylist**の型定義については、「」を参照してください。 
    
 _/オプション_
  
- 順番**UPS_THESE_FOLDERS**が設定されている場合、 *pel*内の対応するフォルダーのフォルダオプションの配列です。 これらのフォルダーオプションは、「 [upload フォルダーの状態](upload-folder-state.md)」で*pel*にリストされている各フォルダーをアップロードするときに使用されます。 フォルダーオプションの詳細については、「 **[UPFLD](upfld.md)**」を参照してください。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)

