---
title: Office for Android による Android Storage Access Framework のサポート
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office for Android は Android Storage Access Framework と統合され、他のドキュメント プロバイダーが保存したファイルを Office で開けるようにします。
ms.openlocfilehash: dc6478344b19e81fe766412122abec8312ac88e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605499"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Office for Android による Android Storage Access Framework のサポート

Office for Android は Android Storage Access Framework と統合され、他のドキュメント プロバイダーが保存したファイルを Office で開けるようにします。
  
Android 4.4 (API レベル 19) に Storage Access Framework (SAF) が導入されました。SAF を使用することにより、ユーザーはすべての推奨されるドキュメント ストレージ プロバイダー間でドキュメント、イメージ、および他のファイルを参照し、開くことができます。標準の UI によって、ユーザーはアプリおよびプロバイダーの間で一貫した方法で、ファイルの参照およびアクセスができます。
  
## <a name="implement-a-document-provider"></a>ドキュメント プロバイダーを実装する

ドキュメントのストレージ サービスを提供するアプリを開発している場合、[カスタム ドキュメント プロバイダーを記述する](https://developer.android.com/guide/topics/providers/document-provider.html)ことによって、SAF を通じてファイルを利用できるようにします。その後、Office アプリは [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) および [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) インテントを呼び出して、ドキュメント プロバイダーによって返されたファイルを受信できます。インテントには、条件をさらに絞り込むためのフィルターが含まれる場合があることに注意してください。 
  
## <a name="enable-free-consumer-edits"></a>コンシューマーによる無料の編集の有効化

ユーザーは、無料の Microsoft アカウントを使用して Office アプリにサインインし、コンシューマー対象のストレージ サービスに保存されているドキュメントを作成または編集できます。次の表は、Storage Access Framework を通してアクセスされるドキュメントに対するコンシューマーによる無料の編集を有効にするために、プロバイダーがカーソルの一部として提供する必要のある必須プロパティを示します。
  
|**プロパティ**|**Index**|**値**|
|:-----|:-----|:-----|
|ドキュメントの種類  <br/> |com_microsoft_office_doctype  <br/> |\<consumer\>  <br/> |
|サービスのフレンドリ名  <br/> |com_microsoft_office_servicename  <br/> |Office アプリ内の最近使用した一覧にあるドキュメントを特定するのに使用される、サービスのわかりやすい任意の名前。サービスのフレンドり名が表示される前に "使用条件契約" プロパティを指定する必要があることに注意してください。  <br/> |
|使用条件契約  <br/> |com_microsoft_office_termsofuse  <br/> |\<I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Office との統合](integrate-with-office.md)
    
- [コンテンツ プロバイダーの基本](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [コンテンツ プロバイダーの作成](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Storage Access Framework の開発者ガイド](https://developer.android.com/guide/topics/providers/document-provider.html)
    

