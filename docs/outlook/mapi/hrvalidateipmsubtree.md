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
  
標準の個人間メッセージ (IPM) フォルダーをメッセージストアに追加します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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

 _lpmdb_
  
> 順番フォルダーを追加するメッセージストアオブジェクトへのポインター。 
    
 _ulFlags_
  
> 順番フォルダーの作成方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_FORCE_CREATE 
  
> フォルダーは、メッセージストアのプロパティが有効であることを示している場合でも、作成前に確認する必要があります。 クライアントアプリケーションでは、通常、既存のフォルダーの構造が破損していることを示すエラーが発生すると、このフラグが設定されます。 
    
MAPI_FULL_IPM_TREE 
  
> メッセージストアのルートフォルダーに、IPM フォルダーの完全なセットを作成する必要があります。 階層内のフォルダーのタイトルは次のとおりです。
    
    - フォルダービュー
    
    - 共通ビュー
    
    - 検索ルート\*
    
    - IPM サブツリー\*
    
    - Inbox
    
    - 送信トレイ
    
    - 削除済みアイテム\*
    
    - 送信済みアイテム
    
    MAPI_FULL_IPM_TREE フラグが設定され\*ていない場合でも、ここでマークされている3つのフォルダーは、最小セットとして設定されます。 通常、クライアントアプリケーションは、フォルダーを作成するメッセージストアが既定のストアである場合に、このフラグを設定します。
    
 _lpcValues_
  
> [入力]_lppprops_パラメーターで返される配列内の[spropvalue](spropvalue.md)構造体の数へのポインター。 _lppprops_が NULL の場合、 _lpcValues_パラメーターの値は0になります。 
    
 _lppprops_
  
> [入力]**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) プロパティのプロパティ値と、適切なフォルダーエントリ識別子のプロパティを含む**spropvalue**構造体の配列へのポインターへのポインター。 **hrvalidateipmsubtree**がメッセージストア内に受信トレイを作成する場合、 **spropvalue**配列には、という`PROP_TAG(PT_BINARY, PROP_ID_NULL)`特殊なプロパティタグを持つ受信トレイエントリ識別子が含まれます。 _lppprops_パラメーターには NULL を指定できます。これは、呼び出し側の実装では、 **spropvalue**配列を返す必要がないことを示します。 
    
 _lppMapiError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。 **MAPIERROR**構造体が返されない場合、 _lppMAPIError_パラメーターは NULL に設定されます。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

MAPI は、ストアが最初に開かれたとき、またはストアが既定のストアになったときに、メッセージストアの標準の IPM サブツリーを構築するために、 **hrvalidateipmsubtree**関数を内部で使用します。 この関数は、クライアントアプリケーションが標準的なメッセージフォルダーを検証または修復するために使用することもできます。 
  
 **hrvalidateipmsubtree**は、常に、ストアのルートフォルダーおよび [削除済みアイテム] フォルダー内の [ipm サブツリー] フォルダーに、検索ルートと ipm サブツリーのフォルダーを作成します。 [ipm Subtree] サブツリーフォルダーは、そのメッセージストア内の ipm 階層のルートです。 検索ルートフォルダーは、検索結果フォルダーのサブツリーのルートとして使用できます。 
  
ipm クライアントは、ipm サブツリーのルートフォルダーからフォルダー表示を表示し、その下に子フォルダーを表示する必要があります。 メッセージストアのルートフォルダー内の情報は、クライアントのユーザーインターフェイスに表示されません。 この機能は、クライアントが情報を非表示にする必要がある場合に、その情報を IPM サブツリーのルートディレクトリに配置して、ユーザーには表示されないようにすることを意味します。 これに対して、サーバーベースのメッセージストアなど、メッセージやフォルダーをユーザーに対して非表示にする必要がある ipm 以外のアプリケーションは、それらを ipm 階層の外に置くことができます。 
  
 **hrvalidateipmsubtree**は、作成する各 IPM フォルダーに有効なエントリ識別子があるかどうかを示す**PR_VALID_FOLDER_MASK**プロパティを設定します。 メッセージストアの次のエントリ識別子のプロパティは、対応するフォルダーのエントリ識別子に設定され、 **PR_VALID_FOLDER_MASK**と共に_lppprops_パラメーターで返されます。 
  
 **PR_COMMON_VIEWS_ENTRYID**([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID**([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID**([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> IPM 受信トレイのプレースホルダー [PROP_TAG](prop_tag.md) (PT_BINARY、PROP_ID_NULL)。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MstStoreDlg  <br/> |CMsgStoreDlg:: onvalidateipmsubtree  <br/> |mfcmapi は、 **hrvalidateipmsubtree**メソッドを使用して、メッセージストアに標準フォルダーを追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

