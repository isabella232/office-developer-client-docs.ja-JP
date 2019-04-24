---
title: IProfSect imapiprop
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344794"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルセクションオブジェクトのプロパティと共に動作します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|公開者:  <br/> |Profile section オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IProfSect  <br/> |
|ポインターの種類:  <br/> |LPPROFSECT  <br/> |
|トランザクションモデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>v の順序

このインターフェイスには一意のメソッドはありません。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_PROFILE_NAME**([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="notes-to-callers"></a>呼び出し側への注意

**IProfSect**インターフェイスに独自の固有のメソッドはありませんが、プロファイルセクションの[imapiprop](imapipropiunknown.md)メソッドを呼び出すことができます。 **IProfSect**の実装と**imapiprop**の他の実装には、いくつかの相違点があります。
  
- **IProfSect**では、トランザクションモデルはサポートされていません。 
    
- **IProfSect**は、名前付きプロパティをサポートしていません。 
    
- **IProfSect**は、セキュリティで保護されたプロパティに対して、identifier range 0x67f0 を0x67f0 に予約します。 
    
トランザクションモデルをサポートしていないということは、 [imapiprop:: copyprops](imapiprop-copyprops.md)および[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドへの呼び出しの後、プロファイルセクションに加えられたすべての変更が直ちに実行されることを意味します。 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しは成功しますが、変更は実際には保存されません。 
  
途中で発生した変更から保護するために、サービスプロバイダーは、プロパティシートを通じてユーザーに表示されるプロファイルセクションのコピーを作成する必要があります。 プロパティシートは、実際のプロファイルセクションではなく、コピーで使用する必要があります。 ユーザーが **[OK** ] ボタンをクリックして変更が正確であることを確認すると、変更内容を [実際のプロファイル] セクションに保存することができます。 
  
[コピーされたプロファイル] セクションを使用してプロパティシートを実装するには、次の手順を使用します。
  
1. [imapisupport:: openプロファイル](imapisupport-openprofilesection.md)のセクションまたは[IProviderAdmin:: openprofile](iprovideradmin-openprofilesection.md)の開始方法を呼び出すことによって、プロファイルセクションを開きます。 
    
2. [createiprop](createiprop.md)関数を呼び出して、プロパティデータオブジェクト ( **ipropdata**インターフェイスをサポートするオブジェクト) を取得します。 
    
3. プロファイルセクションの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、プロパティシートに表示されるプロパティをプロファイルセクションからプロパティデータオブジェクトにコピーします。 
    
4. [imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出して、サービスプロバイダーにプロパティシートが表示されるように要求し、 _lpconfigdata_パラメーターのプロパティデータオブジェクトへのポインターを渡します。 
    
5. ユーザーがプロパティシートの構成プロパティに加えた変更を保存するときには、 [imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、プロパティデータオブジェクトからプロファイルセクションにプロパティをコピーして戻します。 
    
プロファイルセクションは、他のオブジェクトとは異なり、名前付きプロパティをサポートしていません。 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)および[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドは、プロファイルセクションオブジェクトで呼び出された場合、MAPI_E_NO_SUPPORT を返します。 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用して、0x8000 を超える範囲のプロパティ識別子を設定すると、PT_ERROR プロパティの型が返されます。 
  
プロファイルセクションでは、セキュリティで保護されたプロパティに対して識別子範囲0x67f0 から0x67f0 を予約します。 サービスプロバイダーは、この範囲を使用して、パスワードやその他のプロバイダー固有の資格情報を格納できます。 この範囲内のプロパティは、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドの_lpPropTag_パラメーターで NULL が渡されたときに、プロパティの完全な一覧に返されません。 __ または、 [imapiprop:: getproplist](imapiprop-getproplist.md)メソッド。 セキュリティで保護されたプロパティは、識別子によって明示的に要求する必要があります。 
  
MAPI furnishes は、ハードコードされた定数 MUID_PROFILE_INSTANCE を持つプロファイルセクションを識別子として、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) を1つのプロパティとして使用します。 MAPI を使用すると、作成されたすべてのプロファイルで**PR_SEARCH_KEY**プロパティの値が一意になることが保証されます。 一意性が重要な場合は、 **PR_PROFILE_NAME**の代わりに**PR_SEARCH_KEY**を使用します。これは、削除されたプロファイルの後に同じ名前の別のプロファイルが続く可能性があるためです。 
  
プロファイルセクションの使用方法の詳細については、「[プロファイルおよびメッセージサービスを管理](administering-profiles-and-message-services.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

