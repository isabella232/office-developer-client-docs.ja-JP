---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c13ab9ce9c2564c39bfe9b2689f05439bc7b74ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800445"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**適用対象**: Outlook 
  
コンテナーで、さらにアクセスするためのインターフェイス ポインターを返すには、オブジェクトを開きます。
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはオブジェクトのエントリの識別子へのポインター。 _LpEntryID_は、NULL に設定されている場合は、コンテナーの階層の最上位のコンテナーが開かれます。 
    
 _lpInterface_
  
> [in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 パラメーターに NULL が返されるオブジェクトの標準的なインタ フェースの識別子で発生します。 標準的なインタ フェースは、メッセージは、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)です。フォルダーの[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。 標準インターフェイスを使用しているアドレス帳オブジェクト[IDistList: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[IMailUser: IMAPIProp](imailuserimapiprop.md)メッセージング ユーザーのです。 
    
 _ulFlags_
  
> [in]オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_BEST_ACCESS 
  
> ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を持つオブジェクトが開かれますことを要求します。 たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用アクセスがある場合は、読み取り専用アクセス権を持つオブジェクトを開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> **OpenEntry**を正常に戻す、可能性のあるオブジェクトが呼び出し元のクライアントに完全に利用できる前にするにを使用できます。 オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用のアクセス権を持つオブジェクトが開いているし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
SHOW_SOFT_DELETES
  
> ソフトとしてマークされているアイテムの削除を示しています-は削除済みアイテムの保存に時間の段階です。
    
 _lpulObjType_
  
> [out]開かれているオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開いているオブジェクトへのアクセスに使用するインターフェイスの実装へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーがオブジェクトを開くに十分なアクセス許可を持っているか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開くしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _LpEntryID_で指定されたエントリの識別子は、オブジェクトを表していません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_パラメーターのエントリの識別子は、コンテナーによって認識される形式のではありません。 
    
## <a name="remarks"></a>注釈

**IMAPIContainer::OpenEntry**メソッドは、コンテナー全体にわたってオブジェクトを開き、さらにアクセスに使用するインターフェイスの実装にポインターを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービス プロバイダーが、 _lpInterface_パラメーターにインターフェイス識別子で指定された型のインターフェイスの実装を取得する必要がないために、 _lpulObjType_パラメーターで指定された値を確認します。 必要に応じて、適切な型のポインターに_lppUnk_で返されたポインターにキャストします。 
  
既定では、サービス ・ プロバイダーは MAPI_MODIFY または MAPI_BEST_ACCESS のいずれかのフラグを設定する場合を除き、読み取り専用アクセス権を持つオブジェクトを開きます。 これらのフラグのいずれかを設定すると、サービス ・ プロバイダーは変更可能なオブジェクトを取得しようとします。 ただし、限りませんを変更可能なオブジェクトが開かれているオブジェクトが読み取り/書き込みアクセス許可を要求しました。 どちらか**OpenEntry**によって付与されたアクセス レベルを決定するのにはエラーが発生したり、オブジェクトの**PR_ACCESS_LEVEL**プロパティを取得後に変更されたことを計画します。
  
## <a name="see-also"></a>関連項目



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

