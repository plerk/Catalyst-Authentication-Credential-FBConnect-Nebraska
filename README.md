# Catalyst::Authentication::Credential::FBConnect::Nebraska

Facebook credential for Catalyst::Plugin::Authentication framework.

# SYNOPSIS

In MyApp.pm

    use Catalyst qw/
         Authentication
         Session
         Session::Store::FastMmap
         Session::State::Cookie
    /;

In myapp.conf

    <Plugin::Authentication>
        default_realm   facebook
        <realms>
            <facebook>
                <credential>
                    class       FBConnect::Nebraska
                    api_key     my_app_key
                    secret      my_app_secret
                    app_name    my_app_name
                </credential>
            </facebook>
        </realms>
    </Plugin::Authentication>

In controller code,

    sub facebook : Local {
         my ($self, $c) = @_;

         if( $c->authenticate() ) {
               #do something with $c->user
         }
    }

# DESCRIPTION

This is a fork of the original for my specific application, The Nebraska Project.

# USER METHODS

- $c->user->session\_uid
- $c->user->session\_key
- $c->user->session\_expires

# AUTHOR

Fork by

- Graham Ollis <plicease@cpan.org>

Original by

- Cosmin Budrica <cosmin@sinapticode.com>
- Bogdan Lucaciu <bogdan@sinapticode.com>
- With contributions from:

    Tomas Doran <bobtfish@bobtfish.net>

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2009 by Sinapticode.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
