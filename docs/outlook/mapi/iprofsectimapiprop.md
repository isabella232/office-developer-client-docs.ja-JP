---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3046e8e71af92015ca5fd40e8a81c2afa8db89ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571571"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル セクション オブジェクトのプロパティを操作します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|次のユーザーによって公開されます。  <br/> |プロファイル セクション オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IProfSect  <br/> |
|ポインターの種類:  <br/> |LPPROFSECT  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、一意のメソッドが含まれる必要があります。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="notes-to-callers"></a>呼び出し側への注意

**IProfSect** インターフェイスには独自の一意のメソッドは存在しないが、プロファイル セクションの [IMAPIProp](imapipropiunknown.md)メソッドを呼び出す事が可能です。 **IProfSect** 実装と IMAPIProp の他の実装にはいくつかの違 **いがあります**。
  
- **IProfSect は** トランザクション モデルをサポートしていない。 
    
- **IProfSect では** 、名前付きプロパティはサポートされていません。 
    
- **IProfSect は** 、セキュリティで保護されたプロパティ0x67F0に0x67ff識別子の範囲を予約します。 
    
トランザクション モデルをサポートしていない場合は [、IMAPIProp::CopyProps](imapiprop-copyprops.md) メソッドと [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドの呼び出し後にプロファイル セクションに加えたすべての変更が直ちに行われます。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しは成功しますが、実際には変更は保存しません。 
  
途中で発生する変更から保護するには、サービス プロバイダーは、プロパティ シートを使用してユーザーに表示されるプロファイル セクションのコピーを作成する必要があります。 プロパティ シートは、実際のプロファイル セクションではなく、コピーで動作する必要があります。 ユーザーが **[OK]** ボタンをクリックして変更が正確に行われたか確認すると、変更を実際のプロファイル セクションに保存できます。 
  
コピーしたプロファイル セクションを使用してプロパティ シートを実装するには、次の手順を実行します。
  
1. [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)または[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)メソッドを呼び出して、プロファイル セクションを開きます。 
    
2. [CreateIProp 関数を呼](createiprop.md)び出して、プロパティ データ オブジェクト **(IPropData** インターフェイスをサポートするオブジェクト) を取得します。 
    
3. プロファイル セクションの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、プロパティ シートに表示されるプロパティをプロファイル セクションからプロパティ データ オブジェクトにコピーします。 
    
4. [IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出して、サービス プロバイダーにプロパティ シートの表示を要求し _、lpConfigData_ パラメーターのプロパティ データ オブジェクトへのポインターを渡します。 
    
5. ユーザーがプロパティ シートに構成プロパティの変更を保存する場合は [、IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、プロパティ データ オブジェクトからプロファイル セクションにプロパティをコピーします。 
    
プロファイル セクションは、他のオブジェクトとは異なり、名前付きプロパティをサポートしません。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)および[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドは、プロファイル セクション オブジェクトで呼び出された場合、MAPI_E_NO_SUPPORT を返します。 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用して、0x8000 の上の範囲でプロパティ識別子を設定すると、PT_ERROR プロパティの種類が返されます。 
  
プロファイル セクションでは、セキュリティで保護されたプロパティ0x67F0 0x67FF識別子の範囲を予約します。 サービス プロバイダーは、この範囲を使用して、パスワードや他のプロバイダー固有の資格情報を格納できます。 この範囲のプロパティは [、IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの _lpPropTag_ パラメーターで NULL が渡された場合、プロパティの完全な一覧には返されません。[また、IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドの _lppPropTagArray_ パラメーターでは返されません。 セキュリティで保護されたプロパティは、識別子によって特に要求する必要があります。 
  
MAPI は、ハードコードされた定数を持つプロファイル セクションMUID_PROFILE_INSTANCE識別子として、PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) を単一のプロパティとして指定します。 MAPI を使用すると **、PR_SEARCH_KEYプロパティ** の値が作成されたプロファイルの中で一意になります。 一 **PR_SEARCH_KEY** が重要なPR_PROFILE_NAMEの代わりに、削除されたプロファイルの後に同じ名前の別のプロファイルが続く可能性がある場合に使用します。 
  
プロファイル セクションの使用方法の詳細については、「プロファイルとメッセージ サービスの管理 [」を参照してください](administering-profiles-and-message-services.md)。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

