---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a40046a26efe118e48cdca4749d2e99212bb8bfe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579844"
---
# <a name="sync"></a>SYNC

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ローカル ストアとサーバ間の同期を開始するための情報です。 この情報は、[状態を同期](synchronize-state.md)する際に使用されます。
  
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

## <a name="members"></a>Members

 _ulFlags_
  
- [out]/[in] 同期中の動作を変更する次のフラグのビットマスク。
    
- UPS_UPLOAD_ONLY
    
  - [in]クライアントのみのアップロードを実行します。 Outlook は、ローカルで変更されたフォルダーのみを返します。
    
- UPS_DNLOAD_ONLY
    
  - [in]クライアントは、ダウンロードのみを実行しているが。 Outlook は、フォルダーのアップロードのビットを消去しないでください。
    
- UPS_THESE_FOLDERS
    
  - [in]クライアント同期するフォルダーの指定したセットで指定されたエントリ Id です。 このフラグは、 **UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**のいずれかのフラグを組み合わせることができます。 
    
- UPS_OK
    
  - [out]同期が正常に完了しました。 クライアントがこれをアップロードした後に設定、または完全な同期が完了するとします。
    
- 
    
    > [!NOTE]
    > にもかかわらず、クライアントのアップロードまたは完全に同期できます (アップロード、ダウンロード) フォルダーとアイテムは、レプリケーション API を使用してクライアントが同時にレプリケーションの方向が 1 つだけで*ulFlags*を指定-いずれかの**UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**フラグです。 クライアント、完全な同期の場合、 **UPS_UPLOAD_ONLY**フラグを使用してアップロードし、 **UPS_DNLOAD_ONLY**フラグを指定してダウンロードが最初に行われます。 
  
 _pwzPath_
  
- [out]ローカル ストアへのパス。
    
 _Reserved1_
  
- このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 _Reserved2_
  
- このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 *pel* 
  
- [in]これは、 **UPS_THESE_FOLDERS**が設定されている場合は、同期するフォルダーのエントリ Id の一覧です。 **LPENTRYLIST**の型の定義の mapidefs.h を参照してください。 
    
 _pulFolderOptions_
  
- [in]これは、 **UPS_THESE_FOLDERS**が設定されている場合、 *pel*で対応するフォルダーのフォルダー オプションの配列です。 これらのフォルダーのオプションは、各[フォルダーの状態をアップロード](upload-folder-state.md)する時に*pel*で表示されているフォルダーをアップロードするときに使用されます。 フォルダー オプションの詳細については、 **[UPFLD](upfld.md)** を参照してください。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)

