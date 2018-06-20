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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8b6d4fa1d9ffa6ab5f800bad9f02ac5aa9abd8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800319"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**適用されます**: Outlook 
  
メッセージ ・ ストアには、標準的な個人間メッセージ (IPM) のフォルダーを追加します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parameters

 _lpMDB_
  
> [in]メッセージへのポインターでは、フォルダーを追加するオブジェクトを格納します。 
    
 _ulFlags_
  
> [in]フォルダーを作成する方法を制御するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_FORCE_CREATE 
  
> フォルダーは、メッセージ ・ ストア ・ プロパティの指定が有効である場合でも、作成する前に確認する必要があります。 エラーは、既存のフォルダー構造が破損していることを示す場合、クライアント アプリケーションは通常このフラグを設定します。 
    
MAPI_FULL_IPM_TREE 
  
> IPM フォルダーの完全なセットは、メッセージ ストアのルート フォルダーに作成してください。 階層内のフォルダーのタイトルは次のとおりです。
    
    - フォルダー ビュー
    
    - 共通ビュー
    
    - ルートを検索します。\*
    
    - IPM サブツリー\*
    
    - 受信トレイ
    
    - 送信トレイ
    
    - 削除済みアイテム\*
    
    - 送信済みアイテム
    
    3 つのフォルダーが付いて\*MAPI_FULL_IPM_TREE フラグが設定されていない場合でも作成される最小のセットです。 クライアント アプリケーションは、既定のストアでは、メッセージ ストアのフォルダーが作成されるときに通常このフラグを設定します。
    
 _lpcValues_
  
> [で [チェック アウト]_LppProps_パラメーターで返される配列内の[SPropValue](spropvalue.md)構造体の数へのポインター。 _LppProps_が NULL の場合、 _lpcValues_パラメーターの値は 0 にすることができます。 
    
 _lppProps_
  
> [で [チェック アウト]**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) は、適切なフォルダーのエントリの識別子のプロパティのプロパティ値を含む**SPropValue**構造体の配列へのポインターへのポインター。 **SPropValue**配列にはとしてコード化されたプロパティの特殊なタグで [受信トレイ] のエントリ id が含まれて**HrValidateIPMSubtree**は、メッセージ ・ ストアの受信トレイを作成する場合`PROP_TAG(PT_BINARY, PROP_ID_NULL)`。 _LppProps_のパラメーターには、呼び出し元の実装を**SPropValue**配列が返されることをする必要がないことを示す、NULL を指定できます。 
    
 _lppMapiError_
  
> [out]エラーが発生するバージョン、コンポーネント、およびコンテキストの情報を格納する[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。 **MAPIERROR**構造体が返されない場合、 _lppMAPIError_パラメーターは NULL に設定します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

MAPI は、ストアを最初に開いたとき、またはストアが既定の保存を行った場合、メッセージ ストア内の標準の IPM サブツリーを作成するのには内部的に**HrValidateIPMSubtree**関数を使用します。 この関数は、標準的なメッセージのフォルダーを修復または検証するクライアント アプリケーションによっても使用できます。 
  
 **HrValidateIPMSubtree**は常に、ストアのルート フォルダーと IPM サブツリー フォルダー内の削除済みアイテム フォルダーのルートを検索し、IPM サブツリー フォルダーを作成します。 IPM サブツリー フォルダーは、そのメッセージ ・ ストアに IPM の階層のルートです。 検索のルート フォルダーは、検索結果フォルダーのサブツリーのルートとして使用できます。 
  
IPM のクライアントでは、IPM サブツリーのルート フォルダーから開始し、子の下にあるフォルダーを表示、フォルダーのビューを表示する必要があります。 メッセージ ストアのルート フォルダー内の情報は、クライアントのユーザー インターフェイスに表示されません。 この機能は、クライアントには、情報が非表示にする必要がありますと、情報ことができますが配置される IPM サブツリーのルート ディレクトリに、ユーザーに表示されていないことを示します。 一方、IPM 以外のアプリケーション、サーバー ベースのメッセージ ・ ストアでは、ユーザーに表示するには、メッセージおよびフォルダーを必要とするまとめることができます IPM 階層に含まれない。 
  
 **HrValidateIPMSubtree**は、各 IPM フォルダーの作成が有効なエントリの識別子を持つかどうかを示すために**PR_VALID_FOLDER_MASK**プロパティを設定します。 メッセージ ・ ストアの次のエントリの識別子プロパティは対応するフォルダーのエントリ id を設定し、 **PR_VALID_FOLDER_MASK**および_lppProps_パラメーターに返されます。 
  
 **PR_COMMON_VIEWS_ENTRYID**([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID**([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID**([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> プレース ホルダー (PT_BINARY, PROP_ID_NULL)、IPM の受信トレイに[PROP_TAG](prop_tag.md) 。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI では、 **HrValidateIPMSubtree**メソッドを使用して、メッセージ ・ ストアに標準的なフォルダーを追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

