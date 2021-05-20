---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436574"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準の対人間メッセージ (IPM) フォルダーをメッセージ ストアに追加します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>パラメーター

 _lpMDB_
  
> [in]フォルダーを追加するメッセージ ストア オブジェクトへのポインター。 
    
 _ulFlags_
  
> [in]フォルダーの作成方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_FORCE_CREATE 
  
> メッセージ ストアのプロパティで有効なフォルダーが示されている場合でも、作成前にフォルダーを確認する必要があります。 通常、クライアント アプリケーションは、既存のフォルダーの構造が破損しているというエラーが表示される場合に、このフラグを設定します。 
    
MAPI_FULL_IPM_TREE 
  
> IPM フォルダーの完全なセットは、メッセージ ストアのルート フォルダーに作成する必要があります。 階層内のフォルダー タイトルは次のとおりです。
    
    - フォルダー ビュー
    
    - 共通ビュー
    
    - 検索ルート\*
    
    - IPM サブツリー\*
    
    - 受信トレイ
    
    - 送信トレイ
    
    - 削除済みアイテム\*
    
    - 送信済みアイテム
    
    ここで、マークされた 3 つのフォルダーは、フラグが設定されていない場合でもMAPI_FULL_IPM_TREE \* 設定されます。 通常、クライアント アプリケーションは、フォルダーを作成するメッセージ ストアが既定のストアである場合に、このフラグを設定します。
    
 _lpcValues_
  
> [in, out]_lppProps_ パラメーターで返される配列内の [SPropValue](spropvalue.md)構造体の数へのポインター。 _lppProps が NULL の場合は、lpcValues_ パラメーターの値を _0_ にできます。 
    
 _lppProps_
  
> [in, out]**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) プロパティおよび適切なフォルダー エントリ識別子プロパティのプロパティ値を含む **SPropValue** 構造体の配列へのポインター。 **HrValidateIPMSubtree** がメッセージ ストアに受信トレイを作成する場合 **、SPropValue** 配列には、 としてコード化された特別なプロパティ タグを持つ受信トレイエントリ識別子が含まれます `PROP_TAG(PT_BINARY, PROP_ID_NULL)` 。 _lppProps_ パラメーターには NULL を指定できます。呼び出し元の実装で **SPropValue** 配列を返す必要がないことを示します。 
    
 _lppMapiError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む [MAPIERROR](mapierror.md) 構造体へのポインターへのポインター。 _MAPIERROR 構造体が返されない場合、lppMAPIError_ パラメーターは **NULL** に設定されます。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

MAPI は **、HrValidateIPMSubtree** 関数を内部的に使用して、ストアを最初に開いた場合、またはストアが既定のストアにされた場合に、メッセージ ストアに標準 IPM サブツリーを作成します。 この関数は、クライアント アプリケーションで標準のメッセージ フォルダーを検証または修復するためにも使用できます。 
  
 **HrValidateIPMSubtree** は常に、ストアのルート フォルダーに検索ルート フォルダーと IPM サブツリー フォルダー、IPM サブツリー フォルダーに [削除済みアイテム] フォルダーを作成します。 IPM サブツリー フォルダーは、そのメッセージ ストア内の IPM 階層のルートです。 検索ルート フォルダーは、検索結果フォルダーのサブツリーのルートとして使用できます。 
  
IPM クライアントは、IPM サブツリー ルート フォルダーから開始し、その下に子フォルダーを表示するフォルダー ビューを表示する必要があります。 メッセージ ストアのルート フォルダー内の情報は、クライアントのユーザー インターフェイスに表示されません。 この機能は、クライアントが情報を非表示にする必要がある場合、情報を IPM サブツリー ルート ディレクトリに置き、ユーザーに表示されない場所に置く可能性を意味します。 これに対し、サーバー ベースのメッセージ ストアなど、メッセージとフォルダーをユーザーに表示しない必要がある IPM 以外のアプリケーションでは、IPM 階層の外側に置く可能性があります。 
  
 **HrValidateIPMSubtree** は **、PR_VALID_FOLDER_MASK** プロパティを設定して、作成する各 IPM フォルダーに有効なエントリ識別子が設定されているかどうかを示します。 メッセージ ストアの次のエントリ識別子プロパティは、対応するフォルダーのエントリ識別子に設定され _、lppProps_ パラメーターと共に次の **PR_VALID_FOLDER_MASK。** 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> IPM 受信 [PROP_TAG](prop_tag.md) のプレースホルダー (PT_BINARY、PROP_ID_NULL)。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI は **、HrValidateIPMSubtree** メソッドを使用して、標準フォルダーをメッセージ ストアに追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

