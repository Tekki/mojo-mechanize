<div>
    <a href="https://travis-ci.com/kiwiroy/mojo-transaction-http-role-mechanize">
      <img src="https://travis-ci.com/kiwiroy/mojo-transaction-http-role-mechanize.svg?branch=master">
    </a>
</div>

# NAME

Mojo::Transaction::HTTP::Role::Mechanize - Mechanize Mojo a little

# SYNOPSIS

    # description
    my $tx = $ua->get('/')->with_roles('+Mechanize');
    my $submit_tx = $tx->submit('#submit-id', username => 'fry');
    $ua->start($submit_tx);

# DESCRIPTION

[Role::Tiny](https://metacpan.org/pod/Role::Tiny) based role to compose a form submission _"trait"_ into
[Mojo::Transaction::HTTP](https://metacpan.org/pod/Mojo::Transaction::HTTP).

# METHODS

[Mojo::Transaction::HTTP::Role::Mechanize](https://metacpan.org/pod/Mojo::Transaction::HTTP::Role::Mechanize) implements the following methods.

## submit

    # result
    $submit_tx = $tx->submit('#id', username => 'fry');

Build a new [Mojo::Transaction::HTTP](https://metacpan.org/pod/Mojo::Transaction::HTTP) object with
["tx" in Mojo::UserAgent::Transactor](https://metacpan.org/pod/Mojo::UserAgent::Transactor#tx) and the contents of the `form` with the
`$id` and merged values.

# AUTHOR

kiwiroy - Roy Storey <kiwiroy@cpan.org>

# LICENSE

This library is free software and may be distributed under the same terms as
perl itself.