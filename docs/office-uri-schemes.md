---
title: Office URI スキーマ
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 834c4d2c2f47c6cc3f35423a7dfe3c13caf3d209
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799277"
---
# <a name="office-uri-schemes"></a>Office URI スキーマ

## <a name="11-abstract"></a>1.1 要約

このドキュメントでは、オフィス生産性向上アプリケーション用の Uniform Resource Identifier (URI) の形式を定義します。このスキームは、Microsoft Office 2010 Service Pack 2 以降でサポートされており、これには Microsoft Office 2013 for Windows および Microsoft SharePoint 2013 などの製品が含まれます。また、Office for iPhone、Office for iPad、および Office for Mac 2011 でもサポートされます。
  
## <a name="12-introduction"></a>1.2 紹介

これらの URI スキームを使用すると、オフィス生産性向上アプリケーションをさまざまなコマンドで呼び出すことができます。各アプリケーションには異なる名前のスキームが与えられますが、すべてのスキームは URI の形式 (URI スキーマ) について同じ規則に従います。
  
## <a name="13-uri-schema"></a>1.3 URI スキーマ

### <a name="full-schema"></a>完全スキーマ

< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  > 
  
このドキュメントで定義する URI には、1 つ以上のコマンド引数を含めることができます。それぞれのコマンド引数には < *command-argument-descriptor*  > と <  *command-argument*  > を含める必要があり、この 2 つの要素を縦線 ("|") 文字で区切る必要があります。URI に 2 つ以上のコマンド引数を含める場合は、各コマンド引数を後続のコマンド引数から分離するために縦線 ("|") 文字を置く必要があります。 
  
これらのスキームには、RFC 3986 のセクション 3.2 で定義されている権限コンポーネントが含まれていません。このドキュメントで規定するコマンドの呼び出しは、コマンド呼び出し元のシステムのコンテキストで実行されます。たとえば、URI "ms-excel:ofv|u|http://contoso/Q4/budget.xls" を、Microsoft Windows と Microsoft Office 2013 がインストールされたパーソナル コンピューターから呼び出した場合の想定される結果は、ローカルにインストールされた Microsoft Excel が起動し、 *http://contoso/Q4/budget.xls*  にあるファイルを読み取り専用モードで開くための引数が渡されることです。なお、この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字には含まれません。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。 
  
スキーム構文に含まれる要素は次のとおりです。
  
1. < *scheme-name*  >: 起動するアプリケーションの種類を示します。たとえば、ms-word: というスキーム名は、Microsoft Word によって登録されています。 
    
2. ":" 区切り文字
    
3. < *command-name*  >: アプリケーションが実行するアクションを記述します。たとえば、表示用にドキュメントを開きます。コマンド名のリストは、セクション 1.5 に記載します。 
    
4. "|" (縦線) 区切り文字
    
5. < *command-argument-descriptor*  >: この要素は、コマンド引数が何を目的としているかについての情報を示します。 
    
6. "|" (縦線) 区切り文字
    
7. < *command-argument*  >: 引数はコマンドによって異なります。よく使用する引数の 1 つはドキュメントへの URI で、通常は http または https スキームを使用します。なお、<  *command-argument*  > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく引数データの一部であるため、エスケープせずに含める必要があることに注意してください。 
    
### <a name="abbreviated-schema"></a>短縮スキーマ

Office URI スキームの短縮形式を使用すると、指定した Office アプリケーションを起動し、指定した URI にあるリソースを開くための短い要求を記述できます。短縮形式では、< *command-name*  > として "ofv"、および <  *command-argument-descriptor*  > として "u" が暗黙的に指定されます。このスキーマでは、これ以外のコマンドまたはコマンド引数は指定できません。 
  
< *scheme-name*  >:<  *command-argument*  > 
  
1. < *scheme-name*  >: 起動するアプリケーションの種類を示します。たとえば、ms-word は Microsoft Word を示します。 
    
2. < *command-argument*  >: アプリケーションで開くリソースの URI を指定します。現在のところ、http または https スキームに基づく URI のみがサポートされています。 
    
## <a name="14-scheme-names-and-office-application-registrations"></a>1.4 スキーム名と Office アプリケーションの登録

次のリストは、Microsoft Office アプリケーションで実装されるスキーム名です。Microsoft Office をインストールすると、各スキーム名が Windows に登録され、同じ名前の Office 製品によって処理されるようになります。"ms-spd" は SharePoint Designer の省略形です。
  
> - *ms-word:* 
    
> - *ms-powerpoint:* 
    
> - *ms-excel:* 
    
> - *ms-visio:* 
    
> - *ms-access:* 
    
> - *ms-project:* 
    
> - *ms-publisher:* 
    
> - *ms-spd:* 
    
> - *ms-infopath:* 
    
## <a name="15-commands-and-required-command-arguments"></a>1.5 コマンドと必要なコマンド引数

### <a name="view-document"></a>ドキュメントの表示

次のコマンドでは、アプリケーションを起動し、URI で参照されるドキュメントを読み取り専用モードまたは表示モードで開きます。
  
> コマンド名: ofv
    
> コマンド引数記述子: u
    
> コマンド引数: ドキュメントへの URI。http または https スキームに基づいて指定します。
    
> 例:  *ms-excel:ofv|u|http://contoso/Q4/budget.xls* 
    
### <a name="edit-document"></a>ドキュメントの編集

次のコマンドでは、アプリケーションを起動し、URI で参照されるドキュメントを編集モードで開きます。
  
> コマンド名: ofe
    
> コマンド引数記述子: u
    
> コマンド引数: ドキュメントへの URI。http または https スキームに基づいて指定します。
    
> 例:  *ms-powerpoint:ofe|u|http://www.fourthcoffee.com/AllHandsDeck.ppt* 
    
### <a name="new-document-from-template"></a>テンプレートからの新規ドキュメントの作成

次のコマンドでは、アプリケーションを使用して、指定された URI に格納されたテンプレートに基づいて新規ドキュメントを作成し、そのドキュメントを開きます。この処理で、テンプレート ファイルは変更されません。追加のコマンド引数として、ファイルを最初に保存するときの保存場所を示す既定のパスを指定することもできます。ユーザーがこれとは異なる場所を選択することも可能です。
  
> コマンド名: nft
    
> コマンド引数記述子 1: u
    
> コマンド引数 1: テンプレートへの URI。http または https スキームに基づいて指定します。
    
> オプションのコマンド引数記述子 2: s
    
> オプションのコマンド引数 2: 既定の保存フォルダーを示す URI
    
> 例:  *ms-word:nft|u|http://cohowinery/templates/elegance.pot|s|http://cohowinery/presentations* 
    
なお、オプションとして既定の保存場所を指定する場合は、テンプレートと同じホスト名を参照する必要があることに注意してください。
  
さらに、SharePoint Designer アプリケーション (ms-spd: スキームを実装) および InfoPath アプリケーション (ms-infopath: スキームを実装) は、"テンプレートからの新規ドキュメントの作成" 機能をサポートしていません。
  
## <a name="16-backwards-compatibility"></a>1.6 下位互換性

URI を解析して特定のコマンドに該当するコマンド引数を抽出するとき、Office の URI ハンドラーは、想定されるコマンド引数記述子を持つコマンド引数のみを使用します。引数記述子として想定されない引数と引数記述子の追加のペアがある場合、それらの記述子ペアは URI から削除されます。このような仕組みにより、将来のバージョンのスキームでコマンド引数が追加された場合でも、このスキームの古い実装との下位互換性が保たれます。
  
## <a name="17-implementation-restrictions-on-command-arguments"></a>1.7 コマンド引数の実装上の制限

Office 2013 の現在の実装では、コマンド引数に次の制限があります。
  
### <a name="length-limitations-on-uri-command-arguments"></a>URI コマンド引数の長さの制限

URI コマンド引数では、Excel を除くすべてのアプリケーションでパスの長さが最大 256 文字になっています (Excel では 216 文字)。アプリケーションによっては、これより長いパスがサポートされる場合もあります。そのようなサポートに依存するソリューションを展開する場合は、事前にテストすることをお勧めします。
  
### <a name="allowed-characters-in-uri-command-arguments"></a>URI コマンド引数に使用できる文字

許容される URI は、RFC 3987 (Internationalized Resource Identifier (IRI)) で提案されている標準に準拠する必要があります。RFC 3986 で予約されている文字は、パーセントでエンコードするべきでありません。ファイル名に次の文字を含めてはなりません。\ / : ? \< \> | " \*。  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a>付録 A: ms-word スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="a-3-uri-scheme-syntax"></a>A-3. URI スキームの構文

> Word スキーム = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = 開くドキュメントの URI 位置
    
> template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
> save-location = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
### <a name="a-4-uri-scheme-semantics"></a>A-4. URI スキームのセマンティクス

ms-word スキームは、ワード プロセッシング ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことをワード プロセッシング アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことをワード プロセッシング アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをワード プロセッシング アプリケーションに指示します。
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a>A-5. ms-word URI スキームを使用するアプリケーション/プロトコル

ms-word URI スキームは、Microsoft Word 2013 または Microsoft Word 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-word URI を SharePoint ドキュメント ライブラリに格納されたワード プロセッシング ドキュメントへのリンクとして使用します。
  
### <a name="a-6-interoperability-considerations"></a>A-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="a-7-security-considerations"></a>A-7. セキュリティに関する考慮事項

 ms-word URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-word URI へのリンクをクリックすると、登録されたワード プロセッシング アプリケーションが起動し、指定した URI にあるドキュメントを開くようにワード プロセッシング アプリケーションに指示が出されます。ms-word URI を処理するように登録されたワード プロセッシング アプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。 
  
### <a name="a-8-references"></a>A-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a>付録 B: ms-powerpoint スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="b-3-uri-scheme-syntax"></a>B-3. URI スキームの構文

- PowerPoint スキーム = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
- open-for-edit-cmd = "ofe|u|" document-uri
    
- open-for-view-cmd = "ofv|u|" document-uri
    
- new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
- document-uri = 開くドキュメントの URI 位置
    
- template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
- save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
- \*save-location はオプション パラメーターです
    
### <a name="b-4-uri-scheme-semantics"></a>B-4. URI スキームのセマンティクス

ms-powerpoint スキームは、プレゼンテーション ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことをプレゼンテーション アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことをプレゼンテーション アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをプレゼンテーション アプリケーションに指示します。
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a>B-5. ms-powerpoint URI スキームを使用するアプリケーション/プロトコル

ms-powerpoint URI スキームは、Microsoft PowerPoint 2013 または Microsoft PowerPoint 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-powerpoint URI を SharePoint ドキュメント ライブラリに格納されたプレゼンテーション ドキュメントへのリンクとして使用します。
  
### <a name="b-6-interoperability-considerations"></a>B-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="b-7-security-considerations"></a>B-7. セキュリティに関する考慮事項

ms-powerpoint URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-powerpoint URI へのリンクをクリックすると、登録されたプレゼンテーション アプリケーションが起動し、指定した URI にあるドキュメントを開くようにプレゼンテーション アプリケーションに指示が出されます。ms-powerpoint URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="b-8-references"></a>B-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a>付録 C: ms-excel スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="c-3-uri-scheme-syntax"></a>C-3. URI スキームの構文

> Excel スキーム = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = 開くドキュメントの URI 位置
    
> template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
> save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
> \*save-location はオプション パラメーターです
    
### <a name="c-4-uri-scheme-semantics"></a>C-4. URI スキームのセマンティクス

ms-excel スキームは、スプレッドシート ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことをスプレッドシート アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことをスプレッドシート アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをスプレッドシート アプリケーションに指示します。
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a>C-5. ms-excel URI スキームを使用するアプリケーション/プロトコル

ms-excel URI スキームは、Microsoft Excel 2013 または Microsoft Excel 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-excel URI を SharePoint ドキュメント ライブラリに格納されたスプレッドシート ドキュメントへのリンクとして使用します。
  
### <a name="c-6-interoperability-considerations"></a>C-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="c-7-security-considerations"></a>C-7. セキュリティに関する考慮事項

ms-excel URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-excel URI へのリンクをクリックすると、登録されたスプレッドシート アプリケーションが起動し、指定した URI にあるドキュメントを開くようにスプレッドシート アプリケーションに指示が出されます。ms-excel URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="c-8-references"></a>C-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a>付録 D: ms-visio スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="d-3-uri-scheme-syntax"></a>D-3. URI スキームの構文

> Visio スキーム = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = 開くドキュメントの URI 位置
    
> template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
> save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
> \*save-location はオプション パラメーターです
    
### <a name="d-4-uri-scheme-semantics"></a>D-4. URI スキームのセマンティクス

ms-visio スキームは、Microsoft Visio ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Visio に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Visio に指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することを Visio に指示します。
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a>D-5. ms-visio URI スキームを使用するアプリケーション/プロトコル

ms-visio URI スキームは、Microsoft Visio 2013 または Microsoft Visio 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-visio URI を SharePoint ドキュメント ライブラリに格納された Visio ドキュメントへのリンクとして使用します。
  
### <a name="d-6-interoperability-considerations"></a>D-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="d-7-security-considerations"></a>D-7. セキュリティに関する考慮事項

ms-visio URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-visio URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-visio URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="d-8-references"></a>D-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a>付録 E: ms-access スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="e-3-uri-scheme-syntax"></a>E-3. URI スキームの構文

> Access スキーム = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = 開くドキュメントの URI 位置
    
> template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
> save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
> \*save-location はオプション パラメーターです
    
### <a name="e-4-uri-scheme-semantics"></a>E-4. URI スキームのセマンティクス

ms-access スキームは、データベースを開くか作成するための URI 構文を定義します。このスキームでは、参照したデータベース ファイルに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるデータベースを編集用に開くことをデータベース アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるデータベースを読み取り専用モードで開くことをデータベース アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるテンプレートに基づいて新規データベースを作成し、その新規データベースをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをデータベース アプリケーションに指示します。
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a>E-5. ms-access URI スキームを使用するアプリケーション/プロトコル

ms-access URI スキームは、Microsoft Access 2013 または Microsoft Access 2010 Service Pack 2 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-access URI を SharePoint ドキュメント ライブラリに格納された Access データベースへのリンクとして使用します。
  
### <a name="e-6-interoperability-considerations"></a>E-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。\<command-argument\> セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく引数データの一部であるため、エスケープせずに含める必要があることに注意してください。
  
### <a name="e-7-security-considerations"></a>E-7. セキュリティに関する考慮事項

ms-access URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-access URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるデータベースを開くようにアプリケーションに指示が出されます。ms-access URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからデータベースを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="e-8-references"></a>E-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a>付録 F: ms-project スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="f-3-uri-scheme-syntax"></a>F-3. URI スキームの構文

> Project スキーム = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = 開くドキュメントの URI 位置
    
> template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
> save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
> \*save-location はオプション パラメーターです
    
### <a name="f-4-uri-scheme-semantics"></a>F-4. URI スキームのセマンティクス

ms-project スキームは、Microsoft Project ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Project に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Project に指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することを Project に指示します。
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a>F-5. ms-project URI スキームを使用するアプリケーション/プロトコル

ms-project URI スキームは、Microsoft Project 2013 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-project URI を SharePoint ドキュメント ライブラリに格納された Project ドキュメントへのリンクとして使用します。
  
### <a name="f-6-interoperability-considerations"></a>F-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="f-7-security-considerations"></a>F-7. セキュリティに関する考慮事項

ms-project URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-project URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-project URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="f-8-references"></a>F-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a>付録 G: ms-publisher スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="g-3-uri-scheme"></a>G-3. URI スキーム

> Publisher スキーム = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = 開くドキュメントの URI 位置
    
> template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置
    
> save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置
    
> \*save-location はオプション パラメーターです
    
### <a name="g-4-uri-scheme-semantics"></a>G-4. URI スキームのセマンティクス

ms-publisher スキームは、Microsoft Publisher ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Publisher に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Publisher に指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することを Publisher に指示します。
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a>G-5. ms-publisher URI スキームを使用するアプリケーション/プロトコル

ms-publisher URI スキームは、Microsoft Publisher 2013 または Microsoft Publisher 2010 Service Pack 2 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-publisher URI を SharePoint ドキュメント ライブラリに格納された Publisher ドキュメントへのリンクとして使用します。
  
### <a name="g-6-interoperability-considerations"></a>G-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。\<command-argument\> セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく引数データの一部であるため、エスケープせずに含める必要があることに注意してください。
  
### <a name="g-7-security-considerations"></a>G-7. セキュリティに関する考慮事項

ms-publisher URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-publisher URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-publisher URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="g-9-references"></a>G-9. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a>付録 H: ms-spd スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

### <a name="h-3-uri-scheme-syntax"></a>H-3. URI スキームの構文

> SharePoint Designer スキーム = "ms-spd:" open-for-edit-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> document-uri = 開くドキュメントの URI 位置
    
### <a name="h-4-uri-scheme-semantics"></a>H-4. URI スキームのセマンティクス

ms-spd スキームは、Microsoft SharePoint Designer ドキュメントを開くための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 2 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを SharePoint Designer に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを SharePoint Designer に指示します。
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a>H-5. ms-spd URI スキームを使用するアプリケーション/プロトコル

ms-spd URI スキームは、Microsoft SharePoint Designer 2013 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-spd URI を SharePoint ドキュメント ライブラリに格納された SharePoint Designer ドキュメントへのリンクとして使用します。
  
### <a name="h-6-interoperability-considerations"></a>H-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="h-7-security-considerations"></a>H-7. セキュリティに関する考慮事項

ms-spd URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-spd URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-spd URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="h-8-references"></a>H-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a>付録 I: ms-infopath スキームの URI スキーム登録テンプレート
<a name="bk_addresources"> </a>

###   <a name="i-3-uri-scheme-syntax"></a>I-3. URI スキームの構文

> Infopath スキーム = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> document-uri = 開くドキュメントの URI 位置
    
### <a name="i-4-uri-scheme-semantics"></a>I-4. URI スキームのセマンティクス

ms-infopath スキームは、Microsoft Infopath ドキュメントを開いたり、作成したりするための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 2 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Infopath に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Infopath に指示します。
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a>I-5. ms-infopath URI スキームを使用するアプリケーション/プロトコル

ms-infopath URI スキームは、Microsoft Infopath 2013 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-infopath URI を SharePoint ドキュメント ライブラリに格納された Infopath ドキュメントへのリンクとして使用します。
  
### <a name="i-6-interoperability-considerations"></a>I-6. 相互運用性の考慮事項

この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。
  
<*コマンド引数*> 内でセグメントを RFC 3986 の予約文字":"としない区切り記号を引数のデータの一部は、「/」が含まれているためエスケープされていません。 
  
### <a name="i-7-security-considerations"></a>I-7. セキュリティに関する考慮事項

ms-infopath URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-infopath URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-infopath URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。
  
### <a name="i-8-references"></a>I-8. 参照資料

RFC 3987 - International Resource Identifier (IRI)  
  

