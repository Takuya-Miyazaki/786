--------

Hello AWS \.NET community\! Please share your experience and help us improve the AWS SDK for \.NET and its learning resources by [taking a survey](https://amazonmr.au1.qualtrics.com/jfe/form/SV_bqfQLfZ5nhFUiV0)\. This survey takes approximately 10 minute to complete\.

 [ ![\[Image NOT FOUND\]](http://docs.aws.amazon.com/sdk-for-net/v3/developer-guide/images/SurveyButton.png) ](https://amazonmr.au1.qualtrics.com/jfe/form/SV_bqfQLfZ5nhFUiV0)

--------

# Platforms supported by the AWS SDK for \.NET<a name="net-dg-supported-platforms"></a>

The AWS SDK for \.NET provides distinct groups of assemblies for developers to target different platforms\. However, not all SDK functionality is the same on each of these platforms\. This topic describes the differences in support for each platform\.

## \.NET Core<a name="net-core"></a>

The AWS SDK for \.NET supports applications written for \.NET Core\. AWS service clients only support asynchronous calling patterns in \.NET core\. This also affects many of the high level abstractions built on top of service clients like Amazon S3’s `TransferUtility` which will only support asynchronous calls in the \.NET Core environment\.

## \.NET Standard 2\.0<a name="net-standard-2"></a>

Non\-Framework variations of the AWS SDK for \.NET comply with [\.NET Standard 2\.0](https://docs.microsoft.com/en-us/dotnet/standard/net-standard)\.

## \.NET Framework 4\.5<a name="net-dg-platform-diff-netfx45"></a>

\(For full information on \.NET Framework 4\.5 support, see [version 3](../../v3/developer-guide/welcome.html) of the AWS SDK for \.NET Developer Guide\.\)

This version of the AWS SDK for \.NET is compiled against \.NET Framework 4\.5 and runs in the \.NET 4\.0 runtime\. AWS service clients support synchronous and asynchronous calling patterns and use the [async and await](https://docs.microsoft.com/en-us/previous-versions/hh191443(v=vs.140)) keywords introduced in [C\# 5\.0](https://en.wikipedia.org/wiki/C_Sharp_%28programming_language%29#Versions)\.

## \.NET Framework 3\.5<a name="net-dg-platform-diff-winrt"></a>

This version of the AWS SDK for \.NET is compiled against \.NET Framework 3\.5, and runs in either the \.NET 2\.0 or \.NET 4\.0 runtime\. AWS service clients support synchronous and asynchronous calling patterns and use the older Begin and End pattern\.

**Note**  
The AWS SDK for \.NET is not Federal Information Processing Standard \(FIPS\) compliant when used by applications built against version 2\.0 of the CLR\. For details on how you can substitute a FIPS compliant implementation in that environment, refer to [CryptoConfig](https://docs.microsoft.com/en-us/archive/blogs/shawnfa/cryptoconfig) on the Microsoft blog and the [CLR Security](https://github.com/MicrosoftArchive/clrsecurity/) team's HMACSHA256 class \( HMACSHA256Cng \) in Security\.Cryptography\.dll\.

## Portable Class Library and Xamarin<a name="portable-class-library"></a>

The AWS SDK for \.NET also contains a Portable Class Library implementation\. The Portable Class Library implementation can target multiple platforms, including Universal Windows Platform \(UWP\) and Xamarin on iOS and Android\. See the [Mobile SDK for \.NET and Xamarin](https://docs.aws.amazon.com/mobile/sdkforxamarin/developerguide/Welcome.html) for more details\. AWS service clients only support asynchronous calling patterns\.

## Unity support<a name="unity-support"></a>

For information about Unity support, see [Special considerations for Unity support](unity-special.md)\.

## More information<a name="more-info"></a>

[Migrating to version 3\.5 of the AWS SDK for \.NET](net-dg-v35.md)