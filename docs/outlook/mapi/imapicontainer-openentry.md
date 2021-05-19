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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423637"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナー内のオブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]開くオブジェクトのエントリ識別子へのポインター。 _lpEntryID が_ NULL に設定されている場合、コンテナーの階層内のトップ レベル のコンテナーが開きます。 
    
 _lpInterface_
  
> [in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスの識別子が返されます。 メッセージの場合、標準インターフェイスは [IMAPIMessageSite : IUnknown です](imapimessagesiteiunknown.md)。フォルダーの場合 [、IMAPIFolder : IMAPIContainer です](imapifolderimapicontainer.md)。 アドレス帳オブジェクトの標準インターフェイスは、配布リストの [IDistList : IMAPIContainer、](idistlistimapicontainer.md) メッセージング ユーザーの [IMailUser : IMAPIProp](imailuserimapiprop.md) です。 
    
 _ulFlags_
  
> [in]オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセス権を使用してオブジェクトを開く要求。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用アクセス権がある場合は、オブジェクトを読み取り専用アクセスで開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> オブジェクトが呼び出し元のクライアントで完全に利用できる前に **、OpenEntry** が正常に返されるのを許可します。 オブジェクトを使用できない場合は、後続のオブジェクト呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセス権で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。 
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムとしてマークされているアイテム、つまり削除済みアイテムの保持時間フェーズにあるアイテムを表示します。
    
 _lpulObjType_
  
> [out]開いたオブジェクトの型へのポインター。
    
 _lppUnk_
  
> [out]開いているオブジェクトへのアクセスに使用するインターフェイス実装へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーがオブジェクトを開くアクセス許可が不足しているか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開く試みが行われたかのどちらかです。
    
MAPI_E_NOT_FOUND 
  
> _lpEntryID で指定されたエントリ識別子は_、オブジェクトを表すではありません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID_ パラメーターのエントリ識別子は、コンテナーによって認識される形式ではありません。 
    
## <a name="remarks"></a>注釈

**IMAPIContainer::OpenEntry** メソッドは、コンテナー全体でオブジェクトを開き、さらにアクセスするために使用するインターフェイス実装へのポインターを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービス プロバイダーは  _、lpInterface_ パラメーターのインターフェイス識別子で指定された型のインターフェイス実装を返す必要はないので  _、lpulObjType_ パラメーターが指す値を確認します。 必要に応じて  _、lppUnk_ で返されたポインターを適切な型のポインターにキャストします。 
  
既定では、サービス プロバイダーは、読み取り専用のアクセス権を持つオブジェクトを開きます(既定では、MAPI_MODIFYまたはMAPI_BEST_ACCESSします。 これらのフラグの 1 つが設定されている場合、サービス プロバイダーは変更可能なオブジェクトを返します。 ただし、開いたオブジェクトが読み取り/書き込みアクセス許可を持つ変更可能なオブジェクトを要求した場合は、このオブジェクトを想定しなさる必要があります。 後続の変更が失敗する可能性を計画するか、オブジェクトの **PR_ACCESS_LEVEL** プロパティを取得して **、OpenEntry** によって付与されるアクセス レベルを決定します。
  
## <a name="see-also"></a>関連項目



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

