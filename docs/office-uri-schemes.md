---
title: Office URI スキーマ
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 246c1da3647b61c6281c1a52a24826b3f22e5d7e
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293500"
---
# <a name="office-uri-schemes"></a><span data-ttu-id="c3187-102">Office URI スキーマ</span><span class="sxs-lookup"><span data-stu-id="c3187-102">Office URI Schemes</span></span>

## <a name="11-abstract"></a><span data-ttu-id="c3187-103">1.1 要約</span><span class="sxs-lookup"><span data-stu-id="c3187-103">1.1 ABSTRACT</span></span>

<span data-ttu-id="c3187-p101">このドキュメントでは、オフィス生産性向上アプリケーション用の Uniform Resource Identifier (URI) の形式を定義します。このスキームは、Microsoft Office 2010 Service Pack 2 以降でサポートされており、これには Microsoft Office 2013 for Windows および Microsoft SharePoint 2013 などの製品が含まれます。また、Office for iPhone、Office for iPad、および Office for Mac 2011 でもサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c3187-p101">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications. The scheme is supported in Microsoft Office 2010 Service Pack 2 and later, including the Microsoft Office 2013 for Windows and the Microsoft SharePoint 2013 products. It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span>
  
## <a name="12-introduction"></a><span data-ttu-id="c3187-107">1.2 紹介</span><span class="sxs-lookup"><span data-stu-id="c3187-107">1.2 INTRODUCTION</span></span>

<span data-ttu-id="c3187-p102">これらの URI スキームを使用すると、オフィス生産性向上アプリケーションをさまざまなコマンドで呼び出すことができます。各アプリケーションには異なる名前のスキームが与えられますが、すべてのスキームは URI の形式 (URI スキーマ) について同じ規則に従います。</span><span class="sxs-lookup"><span data-stu-id="c3187-p102">These URI schemes allow for office productivity applications to be invoked with various commands. Each application is given a different named scheme but all schemes follow the same rules for how the URI is formed (URI Schema).</span></span>
  
## <a name="13-uri-schema"></a><span data-ttu-id="c3187-110">1.3 URI スキーマ</span><span class="sxs-lookup"><span data-stu-id="c3187-110">1.3 URI SCHEMA</span></span>

### <a name="full-schema"></a><span data-ttu-id="c3187-111">完全スキーマ</span><span class="sxs-lookup"><span data-stu-id="c3187-111">Full schema</span></span>

<span data-ttu-id="c3187-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="c3187-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span></span> 
  
<span data-ttu-id="c3187-p103">このドキュメントで定義する URI には、1 つ以上のコマンド引数を含めることができます。それぞれのコマンド引数には < *command-argument-descriptor*  > と <  *command-argument*  > を含める必要があり、この 2 つの要素を縦線 ("|") 文字で区切る必要があります。URI に 2 つ以上のコマンド引数を含める場合は、各コマンド引数を後続のコマンド引数から分離するために縦線 ("|") 文字を置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p103">A URI as defined in this document may have one or more command arguments, each of which must include both the < *command-argument-descriptor*  > and the <  *command-argument*  > elements and be delimited by the vertical bar ("|") character. When more than one command argument is included in a URI there must be a vertical bar ("|") character separating each command argument from the following command argument.</span></span> 
  
<span data-ttu-id="c3187-p104">これらのスキームには、RFC 3986 のセクション 3.2 で定義されている権限コンポーネントが含まれていません。このドキュメントで規定するコマンドの呼び出しは、コマンド呼び出し元のシステムのコンテキストで実行されます。たとえば、URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" を、Microsoft Windows と Microsoft Office 2013 がインストールされたパーソナル コンピューターから呼び出した場合の想定される結果は、ローカルにインストールされた Microsoft Excel が起動し、 *https://contoso/Q4/budget.xls*  にあるファイルを読み取り専用モードで開くための引数が渡されることです。なお、この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字には含まれません。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p104">These schemes do not include an authority component as defined in section 3.2 of RFC 3986. Invocation of the commands specified in this document takes place in the context of the system invoking the command. For example, when the URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" is invoked from a personal computer running Microsoft Windows with Microsoft Office 2013 installed the expected result is that the local installation of Microsoft Excel will be launched and passed arguments to open the file at  *https://contoso/Q4/budget.xls*  in read-only mode. Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> 
  
<span data-ttu-id="c3187-120">スキーム構文に含まれる要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c3187-120">The scheme syntax includes the following:</span></span>
  
1. <span data-ttu-id="c3187-p105">< *scheme-name*  >: 起動するアプリケーションの種類を示します。たとえば、ms-word: というスキーム名は、Microsoft Word によって登録されています。</span><span class="sxs-lookup"><span data-stu-id="c3187-p105">< *scheme-name*  >: This refers to the type of application that should be invoked. For instance, the ms-word: scheme name is registered by Microsoft Word.</span></span> 
    
2. <span data-ttu-id="c3187-123">":" 区切り文字</span><span class="sxs-lookup"><span data-stu-id="c3187-123">":" separator</span></span>
    
3. <span data-ttu-id="c3187-p106">< *command-name*  >: アプリケーションが実行するアクションを記述します。たとえば、表示用にドキュメントを開きます。コマンド名のリストは、セクション 1.5 に記載します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p106">< *command-name*  >: This describes the actions that the application should perform. For instance, opening a document for viewing. The list of command names is described in section 1.5.</span></span> 
    
4. <span data-ttu-id="c3187-127">"|" (縦線) 区切り文字</span><span class="sxs-lookup"><span data-stu-id="c3187-127">"|" (vertical bar) separator</span></span>
    
5. <span data-ttu-id="c3187-128">< *command-argument-descriptor*  >: この要素は、コマンド引数が何を目的としているかについての情報を示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-128">< *command-argument-descriptor*  >: This element gives more information about what the command argument is about.</span></span> 
    
6. <span data-ttu-id="c3187-129">"|" (縦線) 区切り文字</span><span class="sxs-lookup"><span data-stu-id="c3187-129">"|" (vertical bar) separator</span></span>
    
7. <span data-ttu-id="c3187-p107">< *command-argument*  >: 引数はコマンドによって異なります。よく使用する引数の 1 つはドキュメントへの URI で、通常は http または https スキームを使用します。なお、<  *command-argument*  > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく引数データの一部であるため、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-p107">< *command-argument*  >: The arguments vary depending on the command. One common argument is the URI to a document, typically using the http or https scheme. Note that within <  *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
    
### <a name="abbreviated-schema"></a><span data-ttu-id="c3187-133">短縮スキーマ</span><span class="sxs-lookup"><span data-stu-id="c3187-133">Abbreviated schema</span></span>

<span data-ttu-id="c3187-p108">Office URI スキームの短縮形式を使用すると、指定した Office アプリケーションを起動し、指定した URI にあるリソースを開くための短い要求を記述できます。短縮形式では、< *command-name*  > として "ofv"、および <  *command-argument-descriptor*  > として "u" が暗黙的に指定されます。このスキーマでは、これ以外のコマンドまたはコマンド引数は指定できません。</span><span class="sxs-lookup"><span data-stu-id="c3187-p108">An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema.</span></span> 
  
<span data-ttu-id="c3187-137">< *scheme-name*  >:<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="c3187-137">< *scheme-name*  >:<  *command-argument*  ></span></span> 
  
1. <span data-ttu-id="c3187-p109">< *scheme-name*  >: 起動するアプリケーションの種類を示します。たとえば、ms-word は Microsoft Word を示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p109">< *scheme-name*  >: the type of application that should be invoked. For instance ms-word: for Microsoft Word.</span></span> 
    
2. <span data-ttu-id="c3187-p110">< *command-argument*  >: アプリケーションで開くリソースの URI を指定します。現在のところ、http または https スキームに基づく URI のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c3187-p110">< *command-argument*  >: URI for the resource the application should open. Currently only URIs based on the http or https scheme are supported.</span></span> 
    
## <a name="14-scheme-names-and-office-application-registrations"></a><span data-ttu-id="c3187-142">1.4 スキーム名と Office アプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="c3187-142">1.4 SCHEME NAMES AND OFFICE APPLICATION REGISTRATIONS</span></span>

<span data-ttu-id="c3187-p111">次のリストは、Microsoft Office アプリケーションで実装されるスキーム名です。Microsoft Office をインストールすると、各スキーム名が Windows に登録され、同じ名前の Office 製品によって処理されるようになります。"ms-spd" は SharePoint Designer の省略形です。</span><span class="sxs-lookup"><span data-stu-id="c3187-p111">The following is the list of scheme names implemented in Microsoft Office applications. When Microsoft Office is installed, each scheme name is registered with Windows to be handled by the Office product of the same name. Note that "ms-spd" is an abbreviation for SharePoint Designer.</span></span>
  
> - <span data-ttu-id="c3187-146">*ms-word:*</span><span class="sxs-lookup"><span data-stu-id="c3187-146">*ms-word:*</span></span> 
    
> - <span data-ttu-id="c3187-147">*ms-powerpoint:*</span><span class="sxs-lookup"><span data-stu-id="c3187-147">*ms-powerpoint:*</span></span> 
    
> - <span data-ttu-id="c3187-148">*ms-excel:*</span><span class="sxs-lookup"><span data-stu-id="c3187-148">*ms-excel:*</span></span> 
    
> - <span data-ttu-id="c3187-149">*ms-visio:*</span><span class="sxs-lookup"><span data-stu-id="c3187-149">*ms-visio:*</span></span> 
    
> - <span data-ttu-id="c3187-150">*ms-access:*</span><span class="sxs-lookup"><span data-stu-id="c3187-150">*ms-access:*</span></span> 
    
> - <span data-ttu-id="c3187-151">*ms-project:*</span><span class="sxs-lookup"><span data-stu-id="c3187-151">*ms-project:*</span></span> 
    
> - <span data-ttu-id="c3187-152">*ms-publisher:*</span><span class="sxs-lookup"><span data-stu-id="c3187-152">*ms-publisher:*</span></span> 
    
> - <span data-ttu-id="c3187-153">*ms-spd:*</span><span class="sxs-lookup"><span data-stu-id="c3187-153">*ms-spd:*</span></span> 
    
> - <span data-ttu-id="c3187-154">*ms-infopath:*</span><span class="sxs-lookup"><span data-stu-id="c3187-154">*ms-infopath:*</span></span> 
    
## <a name="15-commands-and-required-command-arguments"></a><span data-ttu-id="c3187-155">1.5 コマンドと必要なコマンド引数</span><span class="sxs-lookup"><span data-stu-id="c3187-155">1.5 COMMANDS AND REQUIRED COMMAND ARGUMENTS</span></span>

### <a name="view-document"></a><span data-ttu-id="c3187-156">ドキュメントの表示</span><span class="sxs-lookup"><span data-stu-id="c3187-156">View Document</span></span>

<span data-ttu-id="c3187-157">次のコマンドでは、アプリケーションを起動し、URI で参照されるドキュメントを読み取り専用モードまたは表示モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="c3187-157">The following command will cause the application to open the document referenced by the URI in a read-only or view mode.</span></span>
  
> <span data-ttu-id="c3187-158">コマンド名: ofv</span><span class="sxs-lookup"><span data-stu-id="c3187-158">Command Name: ofv</span></span>
    
> <span data-ttu-id="c3187-159">コマンド引数記述子: u</span><span class="sxs-lookup"><span data-stu-id="c3187-159">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="c3187-160">コマンド引数: ドキュメントへの URI。http または https スキームに基づいて指定します。</span><span class="sxs-lookup"><span data-stu-id="c3187-160">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="c3187-161">例:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span><span class="sxs-lookup"><span data-stu-id="c3187-161">Example:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span></span> 
    
### <a name="edit-document"></a><span data-ttu-id="c3187-162">ドキュメントの編集</span><span class="sxs-lookup"><span data-stu-id="c3187-162">Edit Document</span></span>

<span data-ttu-id="c3187-163">次のコマンドでは、アプリケーションを起動し、URI で参照されるドキュメントを編集モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="c3187-163">The following command will cause the application to open the document referenced by the URI in editing mode.</span></span>
  
> <span data-ttu-id="c3187-164">コマンド名: ofe</span><span class="sxs-lookup"><span data-stu-id="c3187-164">Command Name: ofe</span></span>
    
> <span data-ttu-id="c3187-165">コマンド引数記述子: u</span><span class="sxs-lookup"><span data-stu-id="c3187-165">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="c3187-166">コマンド引数: ドキュメントへの URI。http または https スキームに基づいて指定します。</span><span class="sxs-lookup"><span data-stu-id="c3187-166">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="c3187-167">例:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span><span class="sxs-lookup"><span data-stu-id="c3187-167">Example:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span></span> 
    
### <a name="new-document-from-template"></a><span data-ttu-id="c3187-168">テンプレートからの新規ドキュメントの作成</span><span class="sxs-lookup"><span data-stu-id="c3187-168">New Document from Template</span></span>

<span data-ttu-id="c3187-p112">次のコマンドでは、アプリケーションを使用して、指定された URI に格納されたテンプレートに基づいて新規ドキュメントを作成し、そのドキュメントを開きます。この処理で、テンプレート ファイルは変更されません。追加のコマンド引数として、ファイルを最初に保存するときの保存場所を示す既定のパスを指定することもできます。ユーザーがこれとは異なる場所を選択することも可能です。</span><span class="sxs-lookup"><span data-stu-id="c3187-p112">The following command will cause the application to create and open a new document based on the template stored at the specified URI. The template file is not modified in this process. An additional command argument may be supplied to specify the default path offered as a save location when the file is first saved. It is possible for the user to choose a different location.</span></span>
  
> <span data-ttu-id="c3187-173">コマンド名: nft</span><span class="sxs-lookup"><span data-stu-id="c3187-173">Command Name: nft</span></span>
    
> <span data-ttu-id="c3187-174">コマンド引数記述子 1: u</span><span class="sxs-lookup"><span data-stu-id="c3187-174">Command argument descriptor 1: u</span></span>
    
> <span data-ttu-id="c3187-175">コマンド引数 1: テンプレートへの URI。http または https スキームに基づいて指定します。</span><span class="sxs-lookup"><span data-stu-id="c3187-175">Command argument 1: a URI to the template, based on the http or https scheme</span></span>
    
> <span data-ttu-id="c3187-176">オプションのコマンド引数記述子 2: s</span><span class="sxs-lookup"><span data-stu-id="c3187-176">Optional Command argument descriptor 2: s</span></span>
    
> <span data-ttu-id="c3187-177">オプションのコマンド引数 2: 既定の保存フォルダーを示す URI</span><span class="sxs-lookup"><span data-stu-id="c3187-177">Optional Command argument 2: URI to specify the default save folder</span></span>
    
> <span data-ttu-id="c3187-178">例:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span><span class="sxs-lookup"><span data-stu-id="c3187-178">Example:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span></span> 
    
<span data-ttu-id="c3187-179">なお、オプションとして既定の保存場所を指定する場合は、テンプレートと同じホスト名を参照する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-179">As a note, if the optional default save location is supplied, it must be pointing to the same host name as the template.</span></span>
  
<span data-ttu-id="c3187-180">さらに、SharePoint Designer アプリケーション (ms-spd: スキームを実装) および InfoPath アプリケーション (ms-infopath: スキームを実装) は、"テンプレートからの新規ドキュメントの作成" 機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c3187-180">Additionally, the SharePoint Designer and InfoPath applications (which implement the ms-spd: scheme and ms-infopath: schemes, respectively) do not support the "new document from template" functionality.</span></span>
  
## <a name="16-backwards-compatibility"></a><span data-ttu-id="c3187-181">1.6 下位互換性</span><span class="sxs-lookup"><span data-stu-id="c3187-181">1.6 BACKWARDS COMPATIBILITY</span></span>

<span data-ttu-id="c3187-p113">URI を解析して特定のコマンドに該当するコマンド引数を抽出するとき、Office の URI ハンドラーは、想定されるコマンド引数記述子を持つコマンド引数のみを使用します。引数記述子として想定されない引数と引数記述子の追加のペアがある場合、それらの記述子ペアは URI から削除されます。このような仕組みにより、将来のバージョンのスキームでコマンド引数が追加された場合でも、このスキームの古い実装との下位互換性が保たれます。</span><span class="sxs-lookup"><span data-stu-id="c3187-p113">When parsing a URI to extract the appropriate command arguments for a given command, the Office URI handler will only use the command arguments that have the expected command argument descriptor. If there are additional pairs of arguments and argument descriptors that have unexpected argument descriptors, they will be removed from the URI. This mechanism allows future versions of the scheme to add additional command arguments without breaking backward compatibility with legacy implementations of this scheme.</span></span>
  
## <a name="17-implementation-restrictions-on-command-arguments"></a><span data-ttu-id="c3187-185">1.7 コマンド引数の実装上の制限</span><span class="sxs-lookup"><span data-stu-id="c3187-185">1.7 IMPLEMENTATION RESTRICTIONS ON COMMAND ARGUMENTS</span></span>

<span data-ttu-id="c3187-186">Office 2013 の現在の実装では、コマンド引数に次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-186">The below restrictions are placed on command arguments in its current implementation in Office 2013.</span></span>
  
### <a name="length-limitations-on-uri-command-arguments"></a><span data-ttu-id="c3187-187">URI コマンド引数の長さの制限</span><span class="sxs-lookup"><span data-stu-id="c3187-187">Length limitations on URI command arguments</span></span>

<span data-ttu-id="c3187-p114">URI コマンド引数では、Excel を除くすべてのアプリケーションでパスの長さが最大 256 文字になっています (Excel では 216 文字)。アプリケーションによっては、これより長いパスがサポートされる場合もあります。そのようなサポートに依存するソリューションを展開する場合は、事前にテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c3187-p114">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.</span></span>
  
### <a name="allowed-characters-in-uri-command-arguments"></a><span data-ttu-id="c3187-190">URI コマンド引数に使用できる文字</span><span class="sxs-lookup"><span data-stu-id="c3187-190">Allowed characters in URI command arguments</span></span>

<span data-ttu-id="c3187-191">許容される URI は、RFC 3987 (Internationalized Resource Identifier (IRI)) で提案されている標準に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-191">Allowed URIs must conform to the standards proposed in RFC 3987 - Internationalized Resource Identifiers (IRIs) .</span></span> <span data-ttu-id="c3187-192">RFC 3986 で予約されている文字は、パーセントでエンコードするべきでありません。</span><span class="sxs-lookup"><span data-stu-id="c3187-192">Characters identified as reserved in RFC 3986 should not be percent encoded.</span></span> <span data-ttu-id="c3187-193">.</span><span class="sxs-lookup"><span data-stu-id="c3187-193">.</span></span> <span data-ttu-id="c3187-194">\ / : ?</span><span class="sxs-lookup"><span data-stu-id="c3187-194">Filenames must not contain any of the following characters: \ / : ?</span></span> <span data-ttu-id="c3187-195">\< \> | " \*。</span><span class="sxs-lookup"><span data-stu-id="c3187-195">\< \> | " or \*.</span></span>  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a><span data-ttu-id="c3187-196">付録 A: ms-word スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-196">APPENDIX A - URI SCHEME REGISTRATION TEMPLATE FOR MS-WORD SCHEME</span></span>
<span data-ttu-id="c3187-197"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-197"><a name="bk_addresources"> </a></span></span>

### <a name="a-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p116">A-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p116">A-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-200">Word スキーム = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-200">Word Scheme = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="c3187-201">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-201">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-202">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-202">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="c3187-204">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-204">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="c3187-205">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-205">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="c3187-206">save-location = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-206">save-location = URI location of folder in which new document should be created</span></span>
    
### <a name="a-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p117">A-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p117">A-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p118">ms-word スキームは、ワード プロセッシング ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことをワード プロセッシング アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことをワード プロセッシング アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをワード プロセッシング アプリケーションに指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p118">The ms-word scheme defines a URI syntax for opening or creating a word processing document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a word processing application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a word processing application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a word processing application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a><span data-ttu-id="c3187-p119">A-5. ms-word URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p119">A-5. Applications/Protocols that use the ms-word URI Scheme</span></span>

<span data-ttu-id="c3187-p120">ms-word URI スキームは、Microsoft Word 2013 または Microsoft Word 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-word URI を SharePoint ドキュメント ライブラリに格納されたワード プロセッシング ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p120">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.</span></span>
  
### <a name="a-6-interoperability-considerations"></a><span data-ttu-id="c3187-p121">A-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p121">A-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p122">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p122">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-220">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-220">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="a-7-security-considerations"></a><span data-ttu-id="c3187-p123">A-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p123">A-7. Security Considerations</span></span>

 <span data-ttu-id="c3187-p124">ms-word URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-word URI へのリンクをクリックすると、登録されたワード プロセッシング アプリケーションが起動し、指定した URI にあるドキュメントを開くようにワード プロセッシング アプリケーションに指示が出されます。ms-word URI を処理するように登録されたワード プロセッシング アプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p124">On systems that have registered handlers to recognize and act on ms-word URIs, clicking on a link to an ms-word URI will cause the registered word processing application to be launched, with instructions to the word processing application to attempt to open a document at the specified URI. Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span> 
  
### <a name="a-8-references"></a><span data-ttu-id="c3187-p125">A-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p125">A-8. References</span></span>

<span data-ttu-id="c3187-227">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-227">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a><span data-ttu-id="c3187-228">付録 B: ms-powerpoint スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-228">APPENDIX B - URI SCHEME REGISTRATION TEMPLATE FOR MS-POWERPOINT SCHEME</span></span>
<span data-ttu-id="c3187-229"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-229"><a name="bk_addresources"> </a></span></span>

### <a name="b-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p126">B-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p126">B-3. URI Scheme Syntax</span></span>

- <span data-ttu-id="c3187-232">PowerPoint スキーム = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-232">PowerPoint Scheme = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
- <span data-ttu-id="c3187-233">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-233">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
- <span data-ttu-id="c3187-234">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-234">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
- <span data-ttu-id="c3187-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
- <span data-ttu-id="c3187-236">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-236">document-uri = URI location of document to open</span></span>
    
- <span data-ttu-id="c3187-237">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-237">template-uri = URI location of template file upon which new file will be based</span></span>
    
- <span data-ttu-id="c3187-238">save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-238">save-location\* = URI location of folder in which new document should be created</span></span>
    
- <span data-ttu-id="c3187-239">\*save-location はオプション パラメーターです</span><span class="sxs-lookup"><span data-stu-id="c3187-239">\*save-location is an optional parameter</span></span>
    
### <a name="b-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p127">B-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p127">B-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p128">ms-powerpoint スキームは、プレゼンテーション ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことをプレゼンテーション アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことをプレゼンテーション アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをプレゼンテーション アプリケーションに指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p128">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a presentation application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a presentation application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a presentation application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a><span data-ttu-id="c3187-p129">B-5. ms-powerpoint URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p129">B-5. Applications/Protocols that use the ms-powerpoint URI Scheme</span></span>

<span data-ttu-id="c3187-p130">ms-powerpoint URI スキームは、Microsoft PowerPoint 2013 または Microsoft PowerPoint 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-powerpoint URI を SharePoint ドキュメント ライブラリに格納されたプレゼンテーション ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p130">The ms-powerpoint URI Scheme is used by Microsoft Office 2013 to invoke Microsoft PowerPoint 2013 or Microsoft PowerPoint 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.</span></span>
  
### <a name="b-6-interoperability-considerations"></a><span data-ttu-id="c3187-p131">B-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p131">B-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p132">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p132">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-253">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-253">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="b-7-security-considerations"></a><span data-ttu-id="c3187-p133">B-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p133">B-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p134">ms-powerpoint URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-powerpoint URI へのリンクをクリックすると、登録されたプレゼンテーション アプリケーションが起動し、指定した URI にあるドキュメントを開くようにプレゼンテーション アプリケーションに指示が出されます。ms-powerpoint URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p134">On systems that have registered handlers to recognize and act on ms-powerpoint URIs, clicking on a link to an ms-powerpoint URI will cause the registered presentation application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="b-8-references"></a><span data-ttu-id="c3187-p135">B-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p135">B-8. References</span></span>

<span data-ttu-id="c3187-260">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-260">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a><span data-ttu-id="c3187-261">付録 C: ms-excel スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-261">APPENDIX C - URI SCHEME REGISTRATION TEMPLATE FOR MS-EXCEL SCHEME</span></span>
<span data-ttu-id="c3187-262"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-262"><a name="bk_addresources"> </a></span></span>

### <a name="c-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p136">C-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p136">C-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-265">Excel スキーム = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-265">Excel Scheme = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="c3187-266">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-266">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-267">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-267">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="c3187-269">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-269">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="c3187-270">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-270">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="c3187-271">save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-271">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="c3187-272">\*save-location はオプション パラメーターです</span><span class="sxs-lookup"><span data-stu-id="c3187-272">\*save-location is an optional parameter</span></span>
    
### <a name="c-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p137">C-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p137">C-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p138">ms-excel スキームは、スプレッドシート ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことをスプレッドシート アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことをスプレッドシート アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをスプレッドシート アプリケーションに指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p138">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a spreadsheet application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a spreadsheet application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a spreadsheet application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a><span data-ttu-id="c3187-p139">C-5. ms-excel URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p139">C-5. Applications/Protocols that use the ms-excel URI Scheme</span></span>

<span data-ttu-id="c3187-p140">ms-excel URI スキームは、Microsoft Excel 2013 または Microsoft Excel 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-excel URI を SharePoint ドキュメント ライブラリに格納されたスプレッドシート ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p140">The ms-excel URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Excel 2013 or Microsoft Excel 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.</span></span>
  
### <a name="c-6-interoperability-considerations"></a><span data-ttu-id="c3187-p141">C-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p141">C-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p142">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p142">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-286">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-286">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="c-7-security-considerations"></a><span data-ttu-id="c3187-p143">C-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p143">C-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p144">ms-excel URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-excel URI へのリンクをクリックすると、登録されたスプレッドシート アプリケーションが起動し、指定した URI にあるドキュメントを開くようにスプレッドシート アプリケーションに指示が出されます。ms-excel URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p144">On systems that have registered handlers to recognize and act on ms-excel URIs, clicking on a link to an ms-excel URI will cause the registered spreadsheet application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="c-8-references"></a><span data-ttu-id="c3187-p145">C-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p145">C-8. References</span></span>

<span data-ttu-id="c3187-293">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-293">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a><span data-ttu-id="c3187-294">付録 D: ms-visio スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-294">APPENDIX D - URI SCHEME REGISTRATION TEMPLATE FOR MS-VISIO SCHEME</span></span>
<span data-ttu-id="c3187-295"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-295"><a name="bk_addresources"> </a></span></span>

### <a name="d-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p146">D-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p146">D-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-298">Visio スキーム = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-298">Visio Scheme = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="c3187-299">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-299">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-300">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-300">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="c3187-302">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-302">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="c3187-303">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-303">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="c3187-304">save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-304">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="c3187-305">\*save-location はオプション パラメーターです</span><span class="sxs-lookup"><span data-stu-id="c3187-305">\*save-location is an optional parameter</span></span>
    
### <a name="d-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p147">D-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p147">D-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p148">ms-visio スキームは、Microsoft Visio ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Visio に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Visio に指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することを Visio に指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p148">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Visio to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a><span data-ttu-id="c3187-p149">D-5. ms-visio URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p149">D-5. Applications/Protocols that use the ms-visio URI Scheme</span></span>

<span data-ttu-id="c3187-p150">ms-visio URI スキームは、Microsoft Visio 2013 または Microsoft Visio 2010 Service Pack 2 を起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-visio URI を SharePoint ドキュメント ライブラリに格納された Visio ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p150">The ms-visio URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Visio 2013 or Microsoft Visio 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.</span></span>
  
### <a name="d-6-interoperability-considerations"></a><span data-ttu-id="c3187-p151">D-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p151">D-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p152">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p152">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-319">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-319">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="d-7-security-considerations"></a><span data-ttu-id="c3187-p153">D-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p153">D-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p154">ms-visio URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-visio URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-visio URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p154">On systems that have registered handlers to recognize and act on ms-visio URIs, clicking on a link to an ms-visio URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="d-8-references"></a><span data-ttu-id="c3187-p155">D-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p155">D-8. References</span></span>

<span data-ttu-id="c3187-326">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-326">RFC 3987 - International Resource Identifiers (IRIs)</span></span>
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a><span data-ttu-id="c3187-327">付録 E: ms-access スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-327">APPENDIX E - URI SCHEME REGISTRATION TEMPLATE FOR MS-ACCESS SCHEME</span></span>
<span data-ttu-id="c3187-328"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-328"><a name="bk_addresources"> </a></span></span>

### <a name="e-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p156">E-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p156">E-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-331">Access スキーム = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-331">Access Scheme = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="c3187-332">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-332">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-333">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-333">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="c3187-335">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-335">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="c3187-336">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-336">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="c3187-337">save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-337">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="c3187-338">\*save-location はオプション パラメーターです</span><span class="sxs-lookup"><span data-stu-id="c3187-338">\*save-location is an optional parameter</span></span>
    
### <a name="e-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p157">E-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p157">E-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p158">ms-access スキームは、データベースを開くか作成するための URI 構文を定義します。このスキームでは、参照したデータベース ファイルに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるデータベースを編集用に開くことをデータベース アプリケーションに指示します。2) open-for-view-cmd (ofv): 指定した URI にあるデータベースを読み取り専用モードで開くことをデータベース アプリケーションに指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるテンプレートに基づいて新規データベースを作成し、その新規データベースをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することをデータベース アプリケーションに指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p158">The ms-access scheme defines a URI syntax for opening or creating a database. The scheme defines three commands that serve as instructions regarding what should be done with the referenced database file. The commands are 1) open-for-edit-cmd (ofe), which instructs the database application to open the database at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs the database application to open the database at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs the database application to create a new database based on the template located at the specified template-uri URI and save the new database either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a><span data-ttu-id="c3187-p159">E-5. ms-access URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p159">E-5. Applications/Protocols that use the ms-access URI Scheme</span></span>

<span data-ttu-id="c3187-p160">ms-access URI スキームは、Microsoft Access 2013 または Microsoft Access 2010 Service Pack 2 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-access URI を SharePoint ドキュメント ライブラリに格納された Access データベースへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p160">The ms-access URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Access 2013 or Microsoft Access 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.</span></span>
  
### <a name="e-6-interoperability-considerations"></a><span data-ttu-id="c3187-p161">E-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p161">E-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-350">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-350">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.</span></span> <span data-ttu-id="c3187-351">これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-351">This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> <span data-ttu-id="c3187-352">セグメント内では \<command-argument\> 、RFC 3986 の予約文字 ":" と "/" は区切り文字ではなく引数データの一部であるため、エスケープせずに含めます。</span><span class="sxs-lookup"><span data-stu-id="c3187-352">Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="e-7-security-considerations"></a><span data-ttu-id="c3187-p163">E-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p163">E-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p164">ms-access URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-access URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるデータベースを開くようにアプリケーションに指示が出されます。ms-access URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからデータベースを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p164">On systems that have registered handlers to recognize and act on ms-access URIs, clicking on a link to an ms-access URI will cause the registered application to be launched, with instructions to the application to attempt to open a database at the specified URI. Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="e-8-references"></a><span data-ttu-id="c3187-p165">E-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p165">E-8. References</span></span>

<span data-ttu-id="c3187-359">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-359">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a><span data-ttu-id="c3187-360">付録 F: ms-project スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-360">APPENDIX F - URI SCHEME REGISTRATION TEMPLATE FOR MS-PROJECT SCHEME</span></span>
<span data-ttu-id="c3187-361"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-361"><a name="bk_addresources"> </a></span></span>

### <a name="f-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p166">F-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p166">F-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-364">Project スキーム = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-364">Project Scheme = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="c3187-365">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-365">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-366">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-366">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="c3187-368">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-368">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="c3187-369">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-369">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="c3187-370">save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-370">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="c3187-371">\*save-location はオプション パラメーターです</span><span class="sxs-lookup"><span data-stu-id="c3187-371">\*save-location is an optional parameter</span></span>
    
### <a name="f-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p167">F-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p167">F-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p168">ms-project スキームは、Microsoft Project ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Project に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Project に指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することを Project に指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p168">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Project to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Project to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Project to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a><span data-ttu-id="c3187-p169">F-5. ms-project URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p169">F-5. Applications/Protocols that use the ms-project URI Scheme</span></span>

<span data-ttu-id="c3187-p170">ms-project URI スキームは、Microsoft Project 2013 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-project URI を SharePoint ドキュメント ライブラリに格納された Project ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p170">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.</span></span>
  
### <a name="f-6-interoperability-considerations"></a><span data-ttu-id="c3187-p171">F-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p171">F-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p172">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p172">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-385">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-385">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="f-7-security-considerations"></a><span data-ttu-id="c3187-p173">F-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p173">F-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p174">ms-project URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-project URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-project URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p174">On systems that have registered handlers to recognize and act on ms-project URIs, clicking on a link to an ms-project URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="f-8-references"></a><span data-ttu-id="c3187-p175">F-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p175">F-8. References</span></span>

<span data-ttu-id="c3187-392">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-392">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a><span data-ttu-id="c3187-393">付録 G: ms-publisher スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-393">APPENDIX G - URI SCHEME REGISTRATION TEMPLATE FOR MS-PUBLISHER SCHEME</span></span>
<span data-ttu-id="c3187-394"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-394"><a name="bk_addresources"> </a></span></span>

### <a name="g-3-uri-scheme"></a><span data-ttu-id="c3187-p176">G-3. URI スキーム</span><span class="sxs-lookup"><span data-stu-id="c3187-p176">G-3. URI Scheme</span></span>

> <span data-ttu-id="c3187-397">Publisher スキーム = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-397">Syntax Publisher Scheme = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="c3187-398">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-398">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-399">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-399">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="c3187-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="c3187-401">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-401">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="c3187-402">template-uri = 新規ファイルの基になるテンプレート ファイルの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-402">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="c3187-403">save-location\* = 新規ドキュメントを作成する先のフォルダーの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-403">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="c3187-404">\*save-location はオプション パラメーターです</span><span class="sxs-lookup"><span data-stu-id="c3187-404">\*save-location is an optional parameter</span></span>
    
### <a name="g-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p177">G-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p177">G-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p178">ms-publisher スキームは、Microsoft Publisher ドキュメントを開くか作成するための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 3 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを Publisher に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを Publisher に指示します。3) new-from-template-cmd (nft): 指定した template-uri URI にあるドキュメント テンプレートに基づいて新規ドキュメントを作成し、その新規ドキュメントをオプションの save-location URI で指定した場所に保存するか、そのオプション URI が指定されていない場合は、既定のドキュメント ライブラリの場所に保存することを Publisher に指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p178">The ms-publisher scheme defines a URI syntax for opening or creating a Microsoft Publisher document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Publisher to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Publisher to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Publisher to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a><span data-ttu-id="c3187-p179">G-5. ms-publisher URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p179">G-5. Applications/Protocols that use the ms-publisher URI Scheme</span></span>

<span data-ttu-id="c3187-p180">ms-publisher URI スキームは、Microsoft Publisher 2013 または Microsoft Publisher 2010 Service Pack 2 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-publisher URI を SharePoint ドキュメント ライブラリに格納された Publisher ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p180">The ms-publisher URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Publisher 2013 or Microsoft Publisher 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.</span></span>
  
### <a name="g-6-interoperability-considerations"></a><span data-ttu-id="c3187-p181">G-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p181">G-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-416">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-416">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.</span></span> <span data-ttu-id="c3187-417">これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-417">This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> <span data-ttu-id="c3187-418">セグメント内では \<command-argument\> 、RFC 3986 の予約文字 ":" と "/" は区切り文字ではなく引数データの一部であるため、エスケープせずに含めます。</span><span class="sxs-lookup"><span data-stu-id="c3187-418">Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="g-7-security-considerations"></a><span data-ttu-id="c3187-p183">G-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p183">G-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p184">ms-publisher URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-publisher URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-publisher URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p184">On systems that have registered handlers to recognize and act on ms-publisher URIs, clicking on a link to an ms-publisher URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-publisher URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="g-9-references"></a><span data-ttu-id="c3187-p185">G-9. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p185">G-9. References</span></span>

<span data-ttu-id="c3187-425">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-425">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a><span data-ttu-id="c3187-426">付録 H: ms-spd スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-426">APPENDIX H - URI SCHEME REGISTRATION TEMPLATE FOR MS-SPD SCHEME</span></span>
<span data-ttu-id="c3187-427"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-427"><a name="bk_addresources"> </a></span></span>

### <a name="h-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p186">H-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p186">H-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-430">SharePoint Designer スキーム = "ms-spd:" open-for-edit-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-430">SharePoint Designer Scheme = "ms-spd:" open-for-edit-cmd</span></span>
    
> <span data-ttu-id="c3187-431">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-431">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-432">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-432">document-uri = URI location of document to open</span></span>
    
### <a name="h-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p187">H-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p187">H-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-p188">ms-spd スキームは、Microsoft SharePoint Designer ドキュメントを開くための URI 構文を定義します。このスキームでは、参照したドキュメントに対して実行する処理に関する指示として次の 2 つのコマンドを定義します。1) open-for-edit-cmd (ofe): 指定した URI にあるドキュメントを編集用に開くことを SharePoint Designer に指示します。2) open-for-view-cmd (ofv): 指定した URI にあるドキュメントを読み取り専用モードで開くことを SharePoint Designer に指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p188">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs SharePoint Designer to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs SharePoint Designer to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a><span data-ttu-id="c3187-p189">H-5. ms-spd URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p189">H-5. Applications/Protocols that use the ms-spd URI Scheme</span></span>

<span data-ttu-id="c3187-p190">ms-spd URI スキームは、Microsoft SharePoint Designer 2013 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-spd URI を SharePoint ドキュメント ライブラリに格納された SharePoint Designer ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p190">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.</span></span>
  
### <a name="h-6-interoperability-considerations"></a><span data-ttu-id="c3187-p191">H-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p191">H-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p192">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p192">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-446">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-446">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="h-7-security-considerations"></a><span data-ttu-id="c3187-p193">H-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p193">H-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p194">ms-spd URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-spd URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-spd URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p194">On systems that have registered handlers to recognize and act on ms-spd URIs, clicking on a link to an ms-spd URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="h-8-references"></a><span data-ttu-id="c3187-p195">H-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p195">H-8. References</span></span>

<span data-ttu-id="c3187-453">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-453">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a><span data-ttu-id="c3187-454">付録 I: ms-infopath スキームの URI スキーム登録テンプレート</span><span class="sxs-lookup"><span data-stu-id="c3187-454">APPENDIX I - URI SCHEME REGISTRATION TEMPLATE FOR MS-INFOPATH SCHEME</span></span>
<span data-ttu-id="c3187-455"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c3187-455"><a name="bk_addresources"> </a></span></span>

###   <a name="i-3-uri-scheme-syntax"></a><span data-ttu-id="c3187-p196">I-3. URI スキームの構文</span><span class="sxs-lookup"><span data-stu-id="c3187-p196">I-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="c3187-458">Infopath スキーム = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span><span class="sxs-lookup"><span data-stu-id="c3187-458">Infopath Scheme = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span></span>
    
> <span data-ttu-id="c3187-459">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-459">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-460">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="c3187-460">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="c3187-461">document-uri = 開くドキュメントの URI 位置</span><span class="sxs-lookup"><span data-stu-id="c3187-461">document-uri = URI location of document to open</span></span>
    
### <a name="i-4-uri-scheme-semantics"></a><span data-ttu-id="c3187-p197">I-4. URI スキームのセマンティクス</span><span class="sxs-lookup"><span data-stu-id="c3187-p197">I-4. URI Scheme Semantics</span></span>

<span data-ttu-id="c3187-464">Ms infopath スキームは、Microsoft Infopath ドキュメントを開く、または作成するための URI 構文を定義します。</span><span class="sxs-lookup"><span data-stu-id="c3187-464">The ms-infopath scheme defines a URI syntax for opening or creating a Microsoft Infopath document.</span></span> <span data-ttu-id="c3187-465">このスキームは、参照されたドキュメントで何を行う必要があるかについての指示として機能する2つのコマンドを定義します。</span><span class="sxs-lookup"><span data-stu-id="c3187-465">The scheme defines two commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="c3187-466">コマンドは 1) open-cmd (ofe) で、編集用に指定された URI でドキュメントを開くよう InfoPath に指示します。および 2) open-cmd (ofv)。これは、指定された URI でドキュメントを読み取り専用モードで開くように InfoPath に指示します。</span><span class="sxs-lookup"><span data-stu-id="c3187-466">The commands are 1) open-for-edit-cmd (ofe), which instructs InfoPath to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs InfoPath to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a><span data-ttu-id="c3187-p199">I-5. ms-infopath URI スキームを使用するアプリケーション/プロトコル</span><span class="sxs-lookup"><span data-stu-id="c3187-p199">I-5. Applications/Protocols that use the ms-infopath URI Scheme</span></span>

<span data-ttu-id="c3187-p200">ms-infopath URI スキームは、Microsoft Infopath 2013 を Web ページから起動するために、Microsoft Office 2013 によって使用されます。Microsoft SharePoint 2013 は、ms-infopath URI を SharePoint ドキュメント ライブラリに格納された Infopath ドキュメントへのリンクとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c3187-p200">The ms-infopath URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Infopath 2013 from web pages. Microsoft SharePoint 2013 uses ms-infopath URIs as links to Infopath documents stored in SharePoint document libraries.</span></span>
  
### <a name="i-6-interoperability-considerations"></a><span data-ttu-id="c3187-p201">I-6. 相互運用性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p201">I-6. Interoperability Considerations</span></span>

<span data-ttu-id="c3187-p202">この仕様で区切り文字として使用している縦線は、RFC 3986 のセクション 2.2 で区切り文字として使用する可能性のある文字として予約されている文字に含まれないことに注意してください。これは、文字をパーセントでエンコードする必要なしに URI コマンド引数でサポートできる文字のセットを最大化するため、意図的に定めたものです。</span><span class="sxs-lookup"><span data-stu-id="c3187-p202">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="c3187-475">< *command-argument* > セグメントの中では RFC 3986 の予約文字である ":" と "/" は区切り文字ではなく、引数データの一部です。したがって、エスケープせずに含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c3187-475">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="i-7-security-considerations"></a><span data-ttu-id="c3187-p203">I-7. セキュリティに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="c3187-p203">I-7. Security Considerations</span></span>

<span data-ttu-id="c3187-p204">ms-infopath URI を認識して動作するように登録されたハンドラーのあるシステムでは、ms-infopath URI へのリンクをクリックすると、登録されたアプリケーションが起動し、指定した URI にあるドキュメントを開くようにアプリケーションに指示が出されます。ms-infopath URI を処理するように登録されたアプリケーションは、悪意のあるコードが含まれている可能性のある、信頼されていないリモート システムからドキュメントを開こうとする操作に対して保護を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3187-p204">On systems that have registered handlers to recognize and act on ms-infopath URIs, clicking on a link to an ms-infopath URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="i-8-references"></a><span data-ttu-id="c3187-p205">I-8. 参照資料</span><span class="sxs-lookup"><span data-stu-id="c3187-p205">I-8. References</span></span>

<span data-ttu-id="c3187-482">RFC 3987 - International Resource Identifier (IRI)</span><span class="sxs-lookup"><span data-stu-id="c3187-482">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
