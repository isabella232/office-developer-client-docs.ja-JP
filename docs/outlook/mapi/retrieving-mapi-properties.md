---
title: MAPI プロパティを取得します。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 41157b97eb28787deaf19c2e974da23dfb77e0be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803765"
---
# <a name="retrieving-mapi-properties"></a>MAPI プロパティを取得します。

 
  
**適用されます**: Outlook 
  
クライアントまたはサービス プロバイダーは、オブジェクトからプロパティを取得、プロパティの値、型、および識別子、オブジェクトに、利用できます。 
  
クライアントとサービス ・ プロバイダーは、次のいずれかを呼び出すことによってオブジェクトのプロパティを取得できます。
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
**GetProps**メソッドを使用して、アクセスの特別なまたは代替のインタ フェースの必要がない 1 つまたは複数のプロパティを取得します。 これは**GetProps**に使用できるプロパティは整数、ブール値など、小さなことを意味します。 
  
 **複数のプロパティを取得するには**
  
1. 取得するプロパティの数を保持するのに十分な大きさ[SPropTagArray](sproptagarray.md)構造体を割り当てます。 
    
2. **あう**、 **SPropTagArray**構造体のメンバーを取得しても、ターゲット プロパティのいずれかの可能な場合は、識別子と型に**aulPropTag**の各メンバーを設定するプロパティの数を設定します。 型が不明な場合は、PT_UNSPECIFIED に設定します。 型と識別子の両方がない既知の場合は、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を呼び出すことによってこの情報を検索します。 **Getproplist メソッド**は、すべてのオブジェクトのサポートされているプロパティを持つプロパティ タグ配列を返します。 プロパティの名前があるのみの場合は、関連付けられている識別子にアクセスする[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出します。 
    
3. プロパティまたはプロパティを開くには、 [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。 
    
**OpenProperty**メソッドを使用して、アクセスの**IStream**または[IMAPITable](imapitableiunknown.md)などの代替のインタ フェースを必要とする大規模なプロパティを開きます。 **OpenProperty**は、通常大きな文字の文字列、バイナリ、およびオブジェクトのプロパティを開くに使用し、のみ 1 つのプロパティを同時に開くことができます。 呼び出し元は、入力パラメーターの 1 つとして要求されるその他のインターフェイスの識別子を渡します。 
  
**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、テキスト ベースのメッセージの本文、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を保持するプロパティを保持するプロパティを開くときは、 **OpenProperty**の一般的な用途のいくつか、OLE オブジェクトまたはメッセージの添付ファイルと**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) は、フォルダーまたはアドレス帳コンテナーの内容テーブルを保持するプロパティです。 
  
プロパティに応じて、 **OpenProperty**から別のインターフェイスが要求されます。 **IStream**をバイトのストリームとして読み書きするプロパティのデータを可能にするインタ フェースは通常、 **PR_BODY**にアクセスするため使用されます。 [IMessage](imessageimapiprop.md)または**IStream**のいずれかが**PR_ATTACH_DATA_OBJ**にアクセスするために使えます。 **IStream**を使用して、TNEF 形式のメッセージは、標準的なメッセージは、埋め込みメッセージの添付ファイルは**IMessage**を使用します。 **PR_CONTAINER_CONTENTS**は、table オブジェクトであるために、 [IMAPITable](imapitableiunknown.md)にアクセスします。
  
 **PR_ATTACH_DATA_BIN プロパティの添付ファイルの取得**
  
1. ファイルのストリームを開く[OpenStreamOnFile](openstreamonfile.md)関数を呼び出します。 
    
2. **IStream**インターフェイスを使用して**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティを取得するメッセージの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)のメソッドを呼び出します。 MAPI_MODIFY とタグの両方のフラグを設定します。 
    
3. **STATSTG**構造体を割り当てるし、そのサイズを決定するファイル ストリームの**IStream::Stat**メソッドの呼び出しで渡すことです。 フラグ STREAM_SEEK_END を使用して**IStream::Seek**を呼び出すには、ストリームのサイズを決定する別の方法です。 
    
4. 添付ファイルのストリームに、ファイルのストリームからデータをコピーするのには、ストリームの**IStream::CopyTo**メソッドを呼び出します。 
    
5. コピー操作が完了すると、それぞれ**が**メソッドを呼び出すことによって両方のストリームを解放します。 
    
**IStream**を使用すると、プロパティへのアクセスのサービス プロバイダーによっては、ストリームでのプロパティのサイズを自動的に送信します。 ストリーム サイズの戻り値のプロパティを開くときに、フラグを遅らせることができます、MAPI_DEFERRED_ERRORS と**OpenProperty**を呼び出すことです。 **IStream::Stat**が、MAPI_DEFERRED_ERRORS と**OpenProperty**フラグを設定した後に、このサイズを取得するために呼び出される場合は、この一連の呼び出しは、余分なリモート プロシージャ呼び出しを強制するためにパフォーマンスが低下します。 パフォーマンスへの影響を避けるためには、クライアントが**OpenProperty**し、**統計値**の呼び出しの間の任意の MAPI メソッドを呼び出すことができます。
  
**OpenProperty**と同様に、 [HrGetOneProp](hrgetoneprop.md)関数は、一度に 1 つのプロパティを開きます。 **HrGetOneProp**は、ローカル マシン上に対象のオブジェクトが存在する場合にのみ使用する必要があります。 対象のオブジェクトをローカルで使用できない場合は、複数のリモート プロシージャ コールとパフォーマンスの低下につながる**HrGetOneProp**を繰り返し使用します。 
  
いくつかのプロパティを必要とする呼び出し元ループ内で**HrGetOneProp**または**OpenProperty**を呼び出すか、 **GetProps**に 1 つの呼び出しを実行します。 **GetProps**を 1 回呼び出すことは、効率的です。 
  
> [!NOTE]
> セキュリティで保護されたプロパティは、 **GetProps**、 **HrGetOneProp**、または**getproplist メソッド**の呼び出しでは、他のプロパティを使用して自動的にご利用いただけません。 セキュリティで保護されたプロパティは、そのプロパティの識別子を使用して明示的に要求する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI Property Overview](mapi-property-overview.md)

