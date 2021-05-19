---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418107"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システム アクセス制御Microsoft Exchange Server(SACL) テーブル オブジェクトおよびルール テーブル オブジェクトへのアクセスをサポートします。Microsoft Exchange Serverします。 このインターフェイスは[IMAPITable : IUnknown](imapitableiunknown.md)インターフェイスに似ているが、SACL とルールを制御するために使用される Microsoft Exchange Server 固有の構造のサポートを追加します。 
  
|||
|:-----|:-----|
|次のユーザーによって公開されます。  <br/> |なし  <br/> |
|実装元:  <br/> |サーバー テーブル オブジェクト  <br/> |
|呼び出し元:  <br/> |MAPI およびクライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IExchangeModifyTable  <br/> |
|ポインターの種類:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|トランザクション モデル:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |テーブル オブジェクトで発生した最後のエラーに関する情報を返します。  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |MAPI テーブル オブジェクトのインターフェイスへのポインターを返します。  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |MAPI テーブル オブジェクトを更新します。  <br/> |
   
|**ルール テーブルの変更に使用されるプロパティ**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
|**SACL テーブルの変更に使用されるプロパティ**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

**IExchangeModifyTable** インターフェイスを取得するには、フォルダー オブジェクトの種類 PT_OBJECT のプロパティで [MAPI IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 **OpenProperty メソッドを呼び出す** 場合は、lpiid パラメーター **IID_IExchangeModifyTable値**_を渡_ します。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

