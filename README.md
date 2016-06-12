# NAME

MojoX::Log::Syslog - Blah blah blah

# SYNOPSIS

    use MojoX::Log::Syslog;

    $app->log( MojoX::Log::Syslog->new(
        facility => 'LOCAL1',
        ident    => 'my_app_name',
        logopt   => 'ndelay,pid'
    ) );

# DESCRIPTION

MojoX::Log::Syslog provies a [Mojo::Log](https://metacpan.org/pod/Mojo::Log) implementation that uses [Sys::Syslog](https://metacpan.org/pod/Sys::Syslog)
as the underlying log mechanism.

## LOG LEVELS

Mojo::Log's fatal() processed same as error() because [Sys::Syslog](https://metacpan.org/pod/Sys::Syslog) doesn't
support that log level.

# ATTRIBUTES

[MojoX::Log::Syslog](https://metacpan.org/pod/MojoX::Log::Syslog) implements the following attributes.

## facility

syslog facility, default to USER

## ident

syslog ident, default to basename($0)

## logopt

syslog logopt, default to 'pid'

# AUTHOR

Fayland Lam <fayland@gmail.com>

# COPYRIGHT

Copyright 2016- Fayland Lam

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
