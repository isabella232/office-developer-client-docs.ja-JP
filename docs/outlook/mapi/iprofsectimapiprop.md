---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c0653caec5f3cac531206e1bb9c4330cac5f3133
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801158"
---
# <a name="iprofsect--imapiprop"></a>IProfSect: IMAPIProp

  
  
**適用されます**: Outlook 
  
プロファイル セクション オブジェクトのプロパティを使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって公開されます。  <br/> |プロファイル セクションのオブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IProfSect  <br/> |
|ポインターの型。  <br/> |LPPROFSECT  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、固有のメソッドがありません。
  
|**必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_PROFILE_NAME**([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="notes-to-callers"></a>呼び出し側への注意

**IProfSect**インターフェイスには、独自の固有のメソッドはありませんが、プロファイル セクションの[IMAPIProp](imapipropiunknown.md)メソッドを呼び出すことができます。 いくつかの違いは、 **IProfSect**の実装と他の**IMAPIProp**の実装があります。
  
- **IProfSect**は、トランザクション モデルをサポートしていません。 
    
- **IProfSect**では、名前付きプロパティはサポートされていません。 
    
- **IProfSect**は、セキュリティで保護されたプロパティの識別子の範囲 0x67F0 に 0x67ff を予約します。 
    
対して行ったすべての変更、プロファイルのセクションで次を呼び出すこと[IMAPIProp::CopyProps](imapiprop-copyprops.md)には、トランザクション モデルをサポートしていないと、 [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドがすぐに発生します。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しは成功ですが、実際に変更を保存できません。 
  
処理の途中で行われる変更から保護するには、サービス プロバイダーは、プロパティ シートを使用してユーザーに表示される自分のプロファイル セクションのコピーを作成する必要があります。 プロパティ シートには、実際のプロファイル セクションではなく、コピーが動作します。 ユーザーは、変更内容が正確であることを確認するのには [ **OK** ] ボタンをクリックすると、ときに、実際のプロファイル セクションに変更を保存できます。 
  
コピー先のプロファイル セクションを使用してプロパティ シートを実装するには、次の手順を使用します。
  
1. [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)または[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)メソッドを呼び出すことによって、[プロファイル] セクションを開きます。 
    
2. プロパティのデータ オブジェクトを取得する[CreateIProp](createiprop.md)関数を呼び出して、 **IPropData**インターフェイスをサポートするオブジェクトです。 
    
3. プロパティのデータ オブジェクトを [プロファイル] セクションのプロパティ シートに表示されるプロパティをコピーするのには、プロファイルのセクションの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。 
    
4. サービス プロバイダーは、プロパティ シートを表示および_lpConfigData_パラメーターのプロパティのデータ オブジェクトへのポインターを渡すことを要求する[IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出します。 
    
5. プロパティ シートで設定のプロパティに変更を保存すると、ときに、プロパティのデータ オブジェクトから、[プロファイル] セクションにプロパティをコピーするのには[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。 
    
他のオブジェクトとは異なり、プロファイルのセクションでは、名前付きプロパティをサポートしていません。 プロファイル セクションのオブジェクトで呼び出される場合、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドと[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドは MAPI_E_NO_SUPPORT を返します。 0x8000 以上の範囲のプロパティの識別子を設定するのには、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用する場合は、PT_ERROR プロパティの型が返されます。 
  
プロファイル セクションでは、セキュリティで保護されたプロパティの識別子の範囲 0x67F0 に 0x67FF を予約します。 サービス プロバイダーは、パスワードおよびその他のプロバイダーに固有の資格情報を格納するのには、この範囲を使用できます。 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの_lpPropTag_パラメーターに NULL が渡されたとき、[の_lppPropTagArray_パラメーターに返される、プロパティの完全なリストでこの範囲内のプロパティは返されませんIMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドです。 セキュリティで保護されたプロパティは、それらの識別子を具体的に要求しなければなりません。 
  
MAPI は、1 つのプロパティとして識別子と定数 MUID_PROFILE_INSTANCE をハード コーディングされた**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) とのプロファイル セクションを提供します。 MAPI は、 **PR_SEARCH_KEY**プロパティの値を作成したすべてのプロファイルの中で一意になることを保証します。 削除するプロファイルを別のプロファイルと同じ名前の後に可能性があるために、一意性が重要では場合は、 **PR_PROFILE_NAME**ではなく**PR_SEARCH_KEY**を使用します。 
  
プロファイルのセクションを使用する方法の詳細については、 [[プロファイルの管理とメッセージ サービス](administering-profiles-and-message-services.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

